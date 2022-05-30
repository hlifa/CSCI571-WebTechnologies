# Homework 6

## Demo (Click on the thumbmail below to view on YouTube)

<a href="https://www.youtube.com/watch?v=HqJl9GOMLkk" target="_blank">
 <img src="https://raw.githubusercontent.com/ruch0401/resources/main/csci-571/basic-stock-search-thumbnail.png" alt="Watch the video for project demo"/>
</a>

## Hands On!

Try the app yourself here - https://basic-stock-search.herokuapp.com/

## Technologies Used

| Area     | Technologies                          |
| -------- | ------------------------------------- |
| Backend  | Python Flask, JSON, Finnhub Stock API |
| Frontend | HTML5, CSS3, Vanilla Javascript       |

## API Endpoints

| Purpose                       | Endpoint                       | Query Params                 | Example                                                                                              |
| ----------------------------- | ------------------------------ | ---------------------------- | ---------------------------------------------------------------------------------------------------- |
| Company Description           | /company-profile           | symbol                       | https://basic-stock-search.herokuapp.com/company-profile?symbol=FB                                                |
| Company Quote       | /quote       | symbol | https://basic-stock-search.herokuapp.com/quote?symbol=FB |
| Company Stock Recommendation    | /company/latest-stock-price    | symbol                       | https://basic-stock-search.herokuapp.com/stock-recommendation?symbol=FB                                        |
| Company Stock Candles          | /stock-candles          | symbol, resolution                            | https://basic-stock-search.herokuapp.com/stock-candles?symbol=FB&resolution=D                                                      |
| Company News                  | /company-news                  | symbol             | https://basic-stock-search.herokuapp.com/company-news?symbol=FB                         |

## Documentation

Click [here](resources/hw6-description.pdf) for HW6 description  
Click [here](resources/hw6-grading.pdf) for HW6 grading guidelines

## Steps to deploy on Heroku

Just as deployment to Google App Engine requires the project to consist of an `app.yaml` file, similarly, deployment to Heroku requires the app to consist of a [Procfile](https://devcenter.heroku.com/articles/procfile). Incase of a Flask app, contents of the Procfile were as follows - 

```
web: gunicorn main:app
```

where `main` = name of the file which runs the Flash app, in my case, it was `main.py`. 

`main.py`
```
if __name__ == '__main__':
    app.run(host='127.0.0.1', port=5000, debug=True)
```

Command to deploy a sub-directory to heroku - `git subtree push --prefix hw6 heroku master`
Note: Command has to be executed from the root of the git repo. `hw6` is the sub-folder, `heroku` is the git remote link to heroku and `master` is the branch on which the deployment needs to take place