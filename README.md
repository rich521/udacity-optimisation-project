## Website Performance Optimization portfolio project

**-----Instructions------**

1. Open 'index.html'
2. Click on 'Cam's Pizzeria' link
3. Scroll down to see the pizzas
4. Click and slide on the scroll bar to choose the size of pizza

**-----index.html------**

Changes made for performance optimization (Results: 92/100):

- inlined style.css (minified)
- removed 'perfmatters.js' and inlined it into index.html
- added a print='media' for print.css
- removed unneccessary link of the google font
- added async for the js script files
- moved the script files to the bottom. Before the end body tag
- reduced size of pizzaia.jpg down to 720x540 and compressed to 67KB


**-----main.js------**

Edit 1 - *(Line:501)*

- Changed loop number 'i' from 200 to 32. Don't need 200 pizzas, 32 is fine.

Edit 2 - *(Line:402)*

- Moved: *var randPizzas = document.querySelectorAll(".randomPizzaContainer");* //Placed on top so that it runs only once


Edit 3 - *(Line:441)*

- Removed: *function determineDx (elem, size){}*
- Removed: *function sizeSwitcher (size){}*

- Replaced as:      *
				    for (var i = 0; i < randPizzas.length; i++) {
				      var newWidth = [25, 33.3, 50];
				      randPizzas[i].style.width = newWidth[size - 1] + "%";
				    }*

Edit 4 - *(Line:496)*

- Moved: *var currentScroll = document.body.scrollTop/1250* out of the loop












