# Instructions

- Run `laravel new <project_name>`
- Run `php artisan install:api` (if on Laravel 10, skip this)
- Create models and database migrations using `php artisan make:model <model_name> -m`
    - This will create a model in app/Models
        - This will be the one to be used to connect in the database within the code
        - Make sure to make the relevant fields fillable (so that no errors occur when trying to add new data for that model)
    - This will also create a migration in database/migrations with timestamp
        - This will be the file containing the columns of your database
        - Run the migration `php artisan migrate:fresh`
- Create controllers using `php artisan make:controller <controller_name> --model=<model_name>`
    - This will be the handler for the business logic of the app
- Add route handlers in routes/api.php
    - If there are no api.php in your routes folder, run `php artisan install:api`
- Always try to run `php artisan optimize` if there are any problems like 500 server error
