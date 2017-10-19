# Laravel 5.5 API Boilerplate Starter
This boilerplate project is created as a starting point for a pure API backend that requires authentication. It was created with a Vue.js SPA in mind but would work with any front end framework/technology.

You can find the Vue.js SPA sister project at [Vue-SPA-Boilerplate-Starter](https://github.com/shealan/Vue-SPA-Boilerplate-Starter)

## Environment
This starter project was created using Vessel; a simple Docker environment even those with little or no Docker experience can use. For more information head over to https://vessel.shippingdocker.com

Note: This project is not tied to Vessel, it will run on Homestead or Valet equally as well, however the installation notes below are geared towards running on Vessel.

### Installation
Clone the project onto your system and follow the steps below.

#### Step 1: Initialise Vessel and Run
```bash
bash vessel init

./vessel start
```
Head to `http://localhost:8001` in your browser and check the site is running.
You can access mySQL on the `3001` port.

#### Step 2: Install Laravel & Define Environment Variables
```bash
./vessel composer install
```
Once composer has installed Laravel and its dependencies copy the variables from the `.env.example` file across to your `.env` file.

#### Step 3: Run Migrations
```bash
./vessel artisan migrate
```
This will setup the database.

#### Step 4: Run Database Seeder
```bash
./vessel artisan db:seed
```
This will add a default user to the database with the following credentials.

```
Name: Example User
Email: example@example.com
Password: password
```
If you wish to change this before running then simply edit the seed data located in the `/database/seeds/UserTableSeeder.php` file.

#### Step 5: Install Passport
```bash
./vessel artisan passport:install
```

## That’s it.
You now have a fully working Laravel 5.5 project with authentication ready to use as a backend. I have included a Paw file in the repository that contains the endpoints for obtaining the key and testing an authenticated endpoint.

If you haven’t used Paw I highly recommend it for API development on the Mac. https://paw.cloud