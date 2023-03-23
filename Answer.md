Solution:-
Bug 1-: can be truely handled by CSS but if we were to make it more flexible, we can evaluate the top, left values of the dropdown parent and the base don that a value to the child or the dropdown can be set, and since the dropdown is a fixed position HTML element, on scroll it will be fixed wrt the viewport, hence we have to make it absolute in order to keep with the inputselectbox. One way it to keep parent element of the dropdown as relative and then positon of dropdown itself as absolute.
Bug 2-: the approve checkbox is hidden because of the display none, hence there won't be any click event visible to the viewport to click on. Hence I have made the checkbox input field as opacity 0 and position absolute superimposing it on the label element. Now we will be able to handle the click event on it.
Bug 3-: In on change event of the inputselect/dropdown, if we check that the employee id is empty then in this case we can load all employee data rather than loading data based on employee id, As the function loadTransactionsByEmployee() gets an invalid employee id, the page crashes.
Bug 4-: Appending existing transactions in the new or load more array in paginated transactions would solve this problem, initially it was adding only view more data from the api.
Bug 5-:Instead of showing that the data is loading on opening the dropdown and clicking on view more, we can use the async methods promise to handle the loading status.
Bug 6-: The viewmore button is only visible iff there is a next page in the pagination. this removes the view more button if the page has reached its end.
Bug 7-:clearCacheByEndpoint(For clearning Cache in order to keep the checkbox changes through the api) on click of the checkbox.

