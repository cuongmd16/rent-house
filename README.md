# rent-house
## _Rent House_

## Installation

Rent House requires [Ruby](https://rubyonrails.org) v3.0.2 to run.

Please install bundle gem then create PostgreSQL user before start the server.

```sh
cd rent-house
bundle install
```

Create postgres user for database migration...

```sh
psql -U postgres
CREATE USER renthouse WITH PASSWORD 'rh@123';
CREATE DATABASE renthouse_development;
GRANT ALL PRIVILEGES ON DATABASE renthouse_development TO renthouse;
exit;
```

Migrate database
```sh
rake db:create
```

To import fake data from seed
```
bundle exec rails ridgepole:seed
```

## Development

Want to contribute? Great!

Make a change in your file and instantaneously see your updates!

Open your favorite Terminal and run these commands.

Before commit your code for new feature or something else, please run rubocop to check coding convention:

```sh
bundle exec rubocop . -A
```