# CSharp Backend Assessment

## Scenario

You are tasked to develop two features in a task board application:

- Create Task: 
    - Here, the user has ability to create a task for himself or other users.
        - A task needs to have a mandatory title and description
            - A title has a maximum of 255 characters
            - A description has a maximum of 5000 characters.
        - The creation date must be automatically calculated
        - Another task can be selected from a list to be its parent task.
            - A task cannot be a parent of its own child
            - A task cannot be a parent of itself
            - A task cannot have "grandchildren"

- Dashboard : 
    - Here, a logged user can view their personal details
        - User name, date when they first joined the app (Format: December 23, 2023), number of tasks (parent tasks only - dont show child tasks) assigned to him/her
    - List of the 10 most recent tasks assigned to them (parent tasks only - do not show child tasks) 
        - The list needs to show a title, a description, the number of child tasks and the date it was created (Format: December 23, 2023)
    - There is an optional date range filter (start/end date) to filter the list by the task's created date. 
    - The user can check/uncheck their task as completed or not.
        - If a parent task is mark as completed, the child tasks must be marked complete as well.
        - If a completed task is then marked incomplete, no need to mark the child tasks as incomplete

        
## Instructions

Build out a REST API and backend to handle the requirements of the features outlined above
applying clean code principles. Keep in mind acronyms such as SOLID, KISS, DRY and YAGNI.


- Do not build a front-end
- Include either the migration files or DDL you used to create the database
- Please use dotnet framework 8.0
- Feel free to use any library
- Do not implement CRUD for users
- Include instructions in the README on how to build and run your solution
- Include automated tests in your solution
- Initialize a local repository (`git init`) and commit as you would a real production project. (No need to push to a remote repo, just local commits will do.)
- I have included a docker-compose file with a Postgres image to make creating the tables and structures needed for this assessment easier, but its not required of you to use it. If you'd rather work with another database provider, feel free to do so. Just make sure to include in the instructions if any steps are required to run it.
- To run the postgres image, you need to install docker and run `docker compose up` and then connect to localhost:5432
    - Any scripts included in the init.sql file will be automatically executed with docker compose up
    - To stop and remove the containers use: `docker compose down`

## Submission

When you're done, please zip your source files (including the .git folder) and email them to brunow@wholechain.com.

Please include (if any) collection files such as swagger.json, postman or insomnia to help run your solution. 

## Help

Feel free to email brunow@wholechain.com if you have any questions.