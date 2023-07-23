
# {{ Mienke Dreyer }} - She Codes News Project

## About This Project

{{ The She Codes News Project is a Django web application that allows users to view, create, and manage news stories. Users can log in to their accounts, create new stories, and view stories published by other users. The project also includes features such as searching for stories by tags, authors or keywords in the articles. Users can also comment on existing articles. }}

## How To Run This Code
{{Clone the repository:
`git clone https://github.com/your-username/she-codes-news.git`
Navigate to the project directory:
`cd she-codes-news`
Create a virtual environment (optional, but recommended):
`python3 -m venv venv`
Activate the virtual environment:
On macOS and Linux:
`source venv/bin/activate`
On Windows:
`venv\Scripts\activate`
Install the required dependencies:
`pip install -r requirements.txt`
Apply database migrations:
`python manage.py migrate`
Create a superuser (admin) account (optional):
`python manage.py createsuperuser`
Run the development server:
`python manage.py runserver`
The application should now be running locally at http://127.0.0.1:8000/
}}

## Database Schema
![ {{ My ERD }} ]( {{ ./relative_path_to_your_entity_relationship_diagram }} 
{{the following entities and relationships can be identified:

CustomUser (User): This entity represents the custom user model which extends the built-in AbstractUser model provided by Django's authentication system. It contains attributes such as username, email, password, etc.

Profile: This entity represents the user profile associated with each CustomUser. It contains attributes like bio, which is a text field to store additional profile information.

NewsStory: This entity represents the news stories created by users. It contains attributes like title, content, publication_date, and a foreign key to the author (CustomUser).

Comment: This entity represents the comments made by users on specific news stories. It contains attributes like text, creation_date, and foreign keys to the commenter (CustomUser) and the story being commented on (NewsStory).

Category: This entity represents the categories that can be assigned to news stories. It contains attributes like name.

The relationships between these entities are as follows:

One CustomUser (User) can have one Profile (One-to-One relationship).
One CustomUser (User) can create multiple NewsStory (One-to-Many relationship).
One CustomUser (User) can write multiple Comment (One-to-Many relationship).
One NewsStory can have multiple Comment (One-to-Many relationship).
One NewsStory can be assigned to multiple Category (Many-to-Many relationship).
}})

## Project Features
[x] Order stories by date![Order stories by date](./images/order_stories_by_date.png)
[x] Styled "new story" form![Styled "new story" form](./images/styled_new_story_form.png)
[x] Story images![Story images](./images/story_images.png)
[x] Log-in/log-out![Log-in/log-out](./images/login_logout.png)
[x] "Account view" page![Account view page](./images/account_view.png)
[x] "Create Account" page![Create Account page](./images/create_account.png)
[x] View stories by author![View stories by author](./images/view_stories_by_author.png)
[x] "Log-in" button only visible when no user is logged in/"Log-out" button only visible when a user *is* logged in![Log-in/out buttons](./images/login_logout_buttons.png)
[x] "Create Story" functionality only available when the user is logged in![Create Story functionality](./images/create_story_functionality.png)

[x] Add tags to the stories and allow the user to search for stories by tags.![Add tags and search](./images/add_tags_and_search.png)
[ ] Add the ability to update and delete stories (consider permissions - who should be allowed to update or and/or delete stories).![Update and delete stories](./images/update_and_delete_stories.png)
[ ] Add the ability to “favourite” stories and see a page with your favourite stories.![Favourite stories](./images/favourite_stories.png)
[ ] Our form for creating stories requires you to add the publication date, update this to automatically save the publication date as the day the story was first published (maybe you could then add a field to show when the story was updated).![Auto-save publication date](./images/auto_save_publication_date.png)
[ ] Gracefully handle the error where someone tries to create a new story when they are not logged in.![Error handling](./images/error_handling.png)

[x] Search button to search by author, keyword, or tag.![Search button](./images/search_button.png)
[x] Add tag button to stories and allow users to search for stories by tag.![Tag button and search](./images/tag_button_and_search.png)
[x] Add the ability to add comments to users' published articles.![Add comments](./images/add_comments.png)
[x] Add the ability to create a user profile, viewing their bio and any articles they have written.![User Profile](./images/user_profile.png)
