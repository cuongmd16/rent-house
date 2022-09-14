rent_house

Rent House


Installation
Accommodation Service requires Ruby v3.0.2 to run.
Please install bundle gem then create PostgreSQL user before start the server.

cd rent_house
bundle install


Create postgres user for database migration...

psql -U postgres
CREATE USER renthouse WITH PASSWORD 'rh@123';
CREATE DATABASE renthouse_development;
GRANT ALL PRIVILEGES ON DATABASE renthouse_development TO renthouse;
exit;


Migrate database

rake db:create


To import fake data from seed


bundle exec rails ridgepole:seed


Development
Want to contribute? Great!
Make a change in your file and instantaneously see your updates!
Open your favorite Terminal and run these commands.
Before commit your code for new feature or something else, please run rubocop to check coding convention:

bundle exec rubocop . -A