# active-class
active class and linking through id


Normally, when we click on the menu of the site, if we have defined the active class inside the corresponding tag, the text will be enlarged without any problem, but when we use the ID to link, it is not possible for us to manually enter it in the HTML code. Let's arrange the class ourselves


const anchor = document.querySelectorAll(".nav-link, .mx-3");
for (let i = 0; i < anchor.length; i++) {
  anchor[i].addEventListener("click", function () {
    for (let i = 0; i < anchor.length; i++) {
      anchor[i].classList.remove("active");
    }
    anchor[i].classList.add("active");
  });
}

