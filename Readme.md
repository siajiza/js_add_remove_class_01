# **How add and remove elements from the html document using javascript.**

**Behavior**

    On the page we´ll watch the text "Hi there", in one color and font-size.
    If we hover with the point mouse over the text, this pointer will change 
    to a small hand that it indicate us to click on there.

    When we click on it, the color and the font-size will change completedly. 
    And if you click on it again, will recover the origin form.

    We part first, from three language code locations;

    -html
    -css 
    -js
    
    Each one are going to contribute with part of the code 
    to create interact between them.

_To find this interact, we need to call with specific class and id names inside of each element, regardless of whether it is html or css. And from javascript we call this elements to the action._

**CSS**

Two different behaviors from each "onclick":

        .activeHeading {
                color: brown;
                font-size: 2em;
                cursor: pointer;
            }

        .nonActiveHeading {
                color: rgb(27, 30, 214);
                font-size: 4em;
                cursor: pointer;
            }

**HTML**

We must use an "id" to manage entire element "div " that in this case will be all the estructure that build the title "Hi There" and, a "class" to focus de behavior that will comes from CSS and show the two differents types of texts.

    <div id="mainHeading" class="activeHeading">
            <h1>Hi there</h1>
    </div>


**JAVASCRIPT**

In this first step we build a variable that contains the entire element "div".

    <script>
        const heading = document.getElementById('mainHeading');

On the second step, we´re gonna build the function on how is gonna change the text. "onclick".


        heading.onclick = () => {
        }
                

On the therd step, we´re gonna build the behavior using the "class" comes from html and the CSS.

            if (heading.classList.contains('activeHeading')) {
                heading.classList.remove('activeHeading');
                heading.classList.add('nonActiveHeading');
            } else {
                heading.classList.remove('nonActiveHeading');
                heading.classList.add('activeHeading');
            }
        }
    </script>






