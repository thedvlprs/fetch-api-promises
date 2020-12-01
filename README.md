[![forthebadge](https://forthebadge.com/images/badges/it-works-why.svg)](https://forthebadge.com)

## Basic code showing how to use Fetch API and Promises

```javascript
const URL = "https://ghibliapi.herokuapp.com/people";
const main = document.getElementById("main");
main.innerHTML = "<p>Loading...";
fetch(URL)
  .then((response) => response.json())
  .then((people) => main.innerHTML = getListOfNames(people));
const getListOfNames = (people) => {
  const names = people
    .map((person) => `<li>${person.name}</li>`)
    .join("\n");
return `<ul>${names}</ul>`;
};```