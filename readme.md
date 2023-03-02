```js
function deleteEmployee(e) {
  fetch(`http://localhost:3000/employees/${e.target.id}`, {
    method: "DELETE",
  })
    .then((response) => response.json())
    .then((json) => console.log("response", json));
}

const deleteCheckboxes = document.querySelector("input[type=checkbox]");
deleteCheckboxes.addEventListener("change", deleteEmployee);
```
