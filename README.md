# Famous-OMDB-Movie-Api

### Build a REST API for us - a movie database interacting with external API.

You can see Project [Click here](https://harshgupta05-omdbmovie-2636.zeet.app/)

## OMDB-MOVIE-API
OMBD-API-bridge is *Proof-of-Concept* project for using (*existing*) and making (*own*) API's in **Django Rest Framework**. It based on external [OMDB-API](http://www.omdbapi.com/) for getting movies and serving them to user of this app in similar form.
Additional features (compare to OMDB-API) of this app are:
* saving all data fetched from OMDB-API to own database ([<u>can be useful, because OMDB-API now has limit of 1000 requests from one API-key</u>](https://www.patreon.com/bePatron?u=5038490))
* add comments to movies existing in database (and also store them in internal database)


## Requirements for endpoints
* **POST */movies*:**
Request body should contain only movie title, and its presence should be validated. Based on passed title, other movie details should be fetched from http://www.omdbapi.com/ (or othersimilar, public movie database) - and saved to application database. Request response should include full movie object, along with all data fetched from external API.
* **GET */movies*:**
Should fetch list of all movies already present in application database.
Additional filtering, sorting is fully optional - but some implementation is a bonus.
* **POST */comments*:**
Request body should contain ID of movie already present in database, and comment text body.
Comment should be saved to application database and returned in request response.
* **GET */comments*:** Should fetch list of all comments present in application database and should allow filtering comments by associated movie, by passing its ID.


## System Requirements

Python 3.9.0

Django 3.2.4



### You can Easily set Up this project locally (manual process) :

FOLLOW THIS STEP :-

1. **Open terminal / command prompt and Clone the project using**

   ```bash
   git clone https://github.com/harshgupta05/omdbmovie.git
   
   ```

2. **Create a virtual environment and Activate** :
 
   On Linux or Mac user put this command -
   ```bash
   virtualenv venv
   ```
    ```bash
    source venv/bin/activate
   ```
   
   Window user put this command :
    ```bash
   virtualenv venv
   ```
    ```bash
    > venv\Scripts\activate
    ```
   

4. **Now Install the dependecies:**

   ```bash
    pip install -r requirements.txt
   ```


5. **Run the `migrate` command:**

   ```bash
   python manage.py migrate
   ```

6. **Start the development server:**

   ```bash
   python manage.py runserver
   ```

7. **Open the browser and go to** [`http://localhost:8000`](http://localhost:8000).


8. **Boom..!! Its Working**


{Note : Rename the `.env.sample` file to `.env`:--   
  Add your all values in `.env` file to run the project without any issues.}


