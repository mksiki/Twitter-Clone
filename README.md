# Twitter-Clone
Basic Twitter User, Tweets clone.

# Flask Twitter API

This project is a Flask-based API that provides functionality for managing user accounts and tweets, including the ability to like tweets. It utilizes Flask SQLAlchemy for database operations and Flask Migrate for database migrations.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Endpoints](#endpoints)
- [Database Seeding](#database-seeding)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. Clone the repository:

   ```bash
   $ git clone https://github.com/your-username/your-project.git
   $ cd your-project
   ```

2. Create a virtual environment and activate it:

   ```bash
   $ python -m venv venv
   $ source venv/bin/activate
   ```

3. Install the required dependencies:

   ```bash
   $ pip install -r requirements.txt
   ```

4. Set up the database:
   - Make sure you have PostgreSQL installed and running.
   - Update the database connection settings in the `create_app` function inside `app.py`:
     ```python
     app.config['SQLALCHEMY_DATABASE_URI'] = 'postgresql://username@localhost:5432/twitter'
     ```
   - Apply the migrations:
     ```bash
     $ flask db upgrade
     ```

## Usage

To start the Flask API, run the following command:

```bash
$ python app.py
```

By default, the API will be accessible at `http://localhost:4999/`.

## Endpoints

The API provides the following endpoints for users:

- **GET /users**: Retrieves a list of all users.
- **GET /users/{id}**: Retrieves information about a specific user.
- **POST /users**: Creates a new user.
- **PUT/PATCH /users/{id}**: Updates a user's information.
- **DELETE /users/{id}**: Deletes a user.
- **GET /users/{id}/liked_tweets**: Retrieves the tweets liked by a user.

The API also provides the following endpoints for tweets:

- **GET /tweets**: Retrieves a list of all tweets.
- **GET /tweets/{id}**: Retrieves information about a specific tweet.
- **POST /tweets**: Creates a new tweet.
- **DELETE /tweets/{id}**: Deletes a tweet.
- **GET /tweets/{id}/liking_users**: Retrieves the users who liked a tweet.

## Database Seeding

The project includes a database seeding script that populates the database with random user accounts and tweets. To run the seeding script, use the following command:

```bash
$ python seed.py
```

The seeding script will generate a specified number of random users and tweets, along with likes randomly distributed among the tweets.

## Contributing

Contributions are welcome! If you would like to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push your changes to your forked repository.
5. Submit a pull request describing your changes.

Please ensure that your code follows the existing style and includes appropriate tests.

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

---
