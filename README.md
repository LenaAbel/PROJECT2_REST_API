# WELCOME ON THE CREATION OF AN API REST! 🔨

## WHAT IS THIS PROJECT ?
&nbsp;&nbsp;The purpose of this project is to create a REST API with NodeJS to serve data from a JSON database.
The database to use in this project is a JSON file that contains information on Nobel Prizes and Nobel Laureates. **(prize.json)**

### TASK TO DO:
- 🚀 Create the API entry point, routers, controllers, and services (or models).
- ✨ 15 features about the laureates, prizes, categories, years...
- ☄️ Swagger documentation to all F1-F15 features. Dedicate the road **/api-docs** for Swagger documentation.

### DATABASE: prize.json
&nbsp;&nbsp;The database to use in this project is a JSON file that contains information on Nobel Prizes and Nobel Laureates. The file name is **prize.json**.
  
*For this project, we cannot:
Convert JSON database to SQL or use NoSQL database. The objective is to become familiar with the use of javascript arrays and filter and search operations.*

### REST API FEATURES
*The API must provide the following functionality:*
- **F1**: List all winners (id, first name, last name).
  - Consider paging.
  - Watch out for duplicates!
- **F2**: Given an identifier, display the winner's information with this ID (first name, last name).
- **F3**: Count the number of prizes offered.
  - Please note that there have been years when no Nobel Prize has been awarded.
  - Pease note that the number of prizes offered is not the same as the number of winners. 
    - **For example in 2021**, 13 people have won Nobel Prizes in Chemistry, Physics, Economics, Peace, medicine and literature. The number of prizes must be 6 (one for each category) and not 13.
- **F4**: Count the number of laureates who received nobel prizes.
  - Watch out for duplicates!!
- **F5**: How many have won more than one Nobel Prize?
  - (first name, last name, number of prizes won)
  - **Ex: Marie Curie, 2**
- **F6**: List all Nobel Prize categories
  - Chemistry, economics, etc.
- **F7**: Determine which category produced the highest number of Nobel laureates.
- **F8**: For each year, indicate how many winners had won a Nobel Prize.
  - **Ex: 2021, 13**
- **F9**: For a given winner ID, display the prizes won (first name, last name, year, category and motivation).
  - **Ex: ID = 6
    - Marie Curie
      - 1911 chemistry in recognition of her services to the…
      - 1903 physics in recognition of the extraordinary services…**
- **F10**: Display all years in which no Nobel Prize was awarded been awarded.
- **F11**: Display all nobel prize years sorted by number of ascending/descending laureates.
  - ?sort=+laureates ⇒ ascending ⇒ start with years with the smallest number of winners
  - ?sort=-laureates ⇒ descending ⇒ start with years with most winners
  - Exclude years when no Nobel Prize was awarded
- **F12**: From first name, or last name, or category, display all winners that match the filter.
  - We should be able to filter by different fields.
- **F13**: Delete a laureate with a given identifier in a year given and a given category.
- **F14**: Update the motivation of a winner with a given identifier in a given year and a given category.
- **F15**: Add a new winner to a given year and category given.
  - If both first and last name exist, use the existing recipient ID. 
    - Otherwise, create a new unique identifier (ex: max(id) + 1).
    
    
 ## VIEWS:
&nbsp;&nbsp;The first view *(http://localhost:3000/list_categories)* consists in creating a model (template) using Handlebars or EJS, in which there is a list
drop-down box with all categories filled in. When the user chooses a category in the list, display all Nobel laureates in this category (first name, last name, year).

![alt text](https://github.com/LenaAbel/PROJECT2_REST_API/blob/main/public/img/LIST_CATEGORIES.png?raw=true)
![alt text](https://github.com/LenaAbel/PROJECT2_REST_API/blob/main/public/img/LIST_CATEGORIES_1.png?raw=true)

&nbsp;&nbsp;The second view *(http://localhost:3000/add_laureates)* create a template using Handlebars or EJS with a form in which you can create a new winner for a given year and category.
- If both first and last name exist, use the existing awardee ID. 
  - Otherwise, create a new unique identifier (ex: max(id) + 1).
- Consider validation middleware.
  - Ex: The user cannot enter a year that does not exist in the JSON file.
  - First name and last name longer than 3 characters. 
  - Motivation not empty
  
![alt text](https://github.com/LenaAbel/PROJECT2_REST_API/blob/main/public/img/LIST_CATEGORIES_1.png?raw=true)
