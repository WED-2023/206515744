[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/89IMDEJr)

## Overview
This is a website intended to represent Edsger dijkstra

I’ve tried to make it as responsive as possible for both mobile and desktop devices. 

For instance, i wrapped the facebook like button in a div and limited its width. I noticed that not doing it overflowed the website box model and allowed the user to scroll to the blank space on the right side of the website.

Elso i stylized the menu so it will appear smalller on mobile, and added a JQuery script (replaced vanilla JS) that will offset the href on screens with width smaller than 600 so the menu will not block the sections title on the page.

```javascript
<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
  <script>
    $(document).ready(function () {
      $("#menu a").click(function (e) {
        e.preventDefault();

        const target = $($(this).attr('href'));
        if (target.length) {
          const offset = window.innerWidth < 600 ? 110 : 70;
          const scrollTo = target.offset().top - offset;

          $('html, body').animate({ scrollTop: scrollTo }, 800);
        }
      });
    });
  </script>
 ```

I.D. 206515744
[github.io page](https://wed-2023.github.io/206515744/)

