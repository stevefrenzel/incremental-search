# Incremental Search
###### This was a project for coding bootcamp [SPICED Academy](https://www.spiced-academy.com/).

<img src="/images/01-incremental-search.png" alt="Incremental Search">

## 1. Description 📖

Every time the user types a visible character, if the current value of the input field is at the beginning of the names of any countries in the list, those country names should be displayed (limit it to four countries displayed at a time).

If the current value of the input is not at the beginning of any of the country names, the string "No results" should be displayed in gray

If a list of results is displayed and the user clicks outside of it and outside of the input field, the result list should disappear.

Result lists should reappear when the user gives the input field focus

If the user mouses over a result in the result list, that result should light up (give it a background color and different text color)

If a result list is displayed and the user hits an up or down arrow key, the appropriate result should light up

If the user clicks a result or hits the enter key while a result is lit up, the full country name of the appropriate result should appear in the input field and the result list should disappear!

## 2. Challenges 🙇

The most challenging part was iterating through the array containing the countries and compare it to the user input:

```javascript
// loop through countries array
for (let i = 0; i < countries.length; i++) {
             // check if letter matches user input
            if (countries[i].toLowerCase().indexOf(val.toLowerCase()) == 0) {
                // push it into matches array
                matches.push(countries[i]);
                // add individual div with object inside to resultsHTML
                resultsHTML += '<div>' + countries[i] + '</div>';
                // limit objects shown to 4
                if (matches.length == 4) {
                    break;
                }
            }
        }
```