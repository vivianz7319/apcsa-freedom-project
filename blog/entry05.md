# Entry 5
##### 5/5/24

So far, my partner and I have completed our MVP. I wouldn't say it was exactly what we hoped it would be, but it is something really close. We have created admin account (username and login), made a html file to create the webpage of the flashcards, created a code that allows user to add decks of flashcards (questions and answers), used arrays to store the flashcards and it also allows them to delete flashcards (delete the array). We didn't make buttons for the answer to show but if you click on the empty space of the card it does show. Since I completed by goal from my last blog entry which is to make an html file to create a web page for our project. My new goal, or I can say our new goal for our next blog entry is to make it more pleasing to the eye and add a few colors into our very empty MVP.

My partner showed me how to install Django into my IDE so our code would work using `python -m pip install django~=5.0` and then whenever I would type `python manage.py runserver` into the terminal it would show us our webpage. Over this month my partner worked in the files I imported last time because she made the login page while I worked on the flashcards. I personally thought the flashcards were very easy until when I tired using the carousel to showcase all the flashcard, it would crash every single time. 

So I did a lot of searching up how would I make a flashcard without using carousel and a lot of the websites I came across really didn't help me, but I came across something similar and I came up with something else using the code that is below: 
```java
var contentArray = localStorage.getItem('items') ? JSON.parse(localStorage.getItem('items')) : [];

document.getElementById("save_card").addEventListener("click", () => {
  addFlashcard();
});

document.getElementById("delete_cards").addEventListener("click", () => {
  localStorage.clear();
  flashcards.innerHTML = '';
  contentArray = [];
});

document.getElementById("show_card_box").addEventListener("click", () => {
  document.getElementById("create_card").style.display = "block";
});

document.getElementById("close_card_box").addEventListener("click", () => {
  document.getElementById("create_card").style.display = "none";
});

flashcardMaker = (text, delThisIndex) => {
  const flashcard = document.createElement("div");
  const question = document.createElement('h2');
  const answer = document.createElement('h2');
  const del = document.createElement('i');

  flashcard.className = 'flashcard';

  question.setAttribute("style", "border-top:1px solid red; padding: 15px; margin-top:30px");
  question.textContent = text.my_question;

  answer.setAttribute("style", "text-align:center; display:none; color:red");
  answer.textContent = text.my_answer;

  del.className = "fas fa-minus";
  del.addEventListener("click", () => {
    contentArray.splice(delThisIndex, 1);
    localStorage.setItem('items', JSON.stringify(contentArray));
    window.location.reload();
  })

  flashcard.appendChild(question);
  flashcard.appendChild(answer);
  flashcard.appendChild(del);

  flashcard.addEventListener("click", () => {
    if(answer.style.display == "none")
      answer.style.display = "block";
    else
      answer.style.display = "none";
  })

  document.querySelector("#flashcards").appendChild(flashcard);
}

contentArray.forEach(flashcardMaker);

addFlashcard = () => {
  const question = document.querySelector("#question");
  const answer = document.querySelector("#answer");

  let flashcard_info = {
    'my_question' : question.value,
    'my_answer'  : answer.value
  }

  contentArray.push(flashcard_info);
  localStorage.setItem('items', JSON.stringify(contentArray));
  flashcardMaker(contentArray[contentArray.length - 1], contentArray.length - 1);
  question.value = "";
  answer.value = "";
}
```
This allowed me to use the flashcard how it is and whenever I press on the empty spaces in the flashcard the word would show. I also made it to like add any card that I would want to asking the user the input and the out put of the flashcard and when the user is done with everything then they can choose to delete all the flashcards. 

After that I pushed everything to my partner and she added all the login information to make our flashcard website work. 

I used many skills during this one month but the two that stood out to me would be collaboration and embracing failure. When I found out that the caursel didn't want to work, I had a very "oh well lets just give up" mindset. Especially when I also have a lot of work for other classes piling up, it was more like I really don't want to do this anymore. I guess I can say I feel a lot better when I was working with my partner, due to the fact that she is working on another part, she is always willing to lend me a hand if I needed it. She showed me support and always try to not stress me out. 

Before the next blog entry, I would like to do the most I can with my MVP, look wise m aking it more pleasing to the eye. But overall, I think my partner and I has meet the requirements of the project and we are both satisfied with what we made.

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
