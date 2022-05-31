# Homework 9 : Stocks - Android App

## Demo (Click on the thumbmail below to view on YouTube)

<a href="https://www.youtube.com/watch?v=FVzIOYYoxWY" target="_blank">
 <img src="https://raw.githubusercontent.com/ruch0401/resources/main/csci-571/stocks-android-app-thumbnail.jpeg" alt="Watch the video for project demo"/>
</a>

## Technologies Used

| Area    | Technologies         |
| ------- | -------------------- |
| Backend | Node.js + Express.js |
| Client  | Android Studio       |

## API Endpoints [Todo]

## Documentation

Click [here](resources/hw9-description.pdf) for HW9 description  
Click [here](resources/hw9-grading.pdf) for HW9 grading guidelines

## Server side code

### Library Details

| Libraries Used | Purpose                                         |
| -------------- | ----------------------------------------------- |
| `axios`        | For making API calls to the Finnhub API         |
| `cors`         | To handle cross-origin-resource-sharing issues  |
| `nodemon`      | For hot reloading of the node server            |
| `express`      | For making use of the Express Node.js framework |

### API endpoints

Host URL1: https://jdofgbmx.uw.r.appspot.com  
Host URL2: https://stock-search-angular.herokuapp.com/

| Purpose                       | Endpoint                       | Query Params                 | Example                                                                                                                   |
| ----------------------------- | ------------------------------ | ---------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| Company Description           | /company/description           | symbol                       | https://stock-search-angular.herokuapp.com/company/description?symbol=AAPL                                                |
| Company Historical Data       | /company/historical/data       | symbol, resolution, from, to | https://stock-search-angular.herokuapp.com/company/historical/data?symbol=AAPL&resolution=D&from=1631022248&to=1631627048 |
| Company Latest Stock Price    | /company/latest-stock-price    | symbol                       | https://stock-search-angular.herokuapp.com/company/latest-stock-price?symbol=AAPL                                         |
| Company Autocomplete          | /company/autocomplete          | q                            | https://stock-search-angular.herokuapp.com/company/autocomplete?q=AA                                                      |
| Company News                  | /company/news                  | symbol, from, to             | https://stock-search-angular.herokuapp.com/company/news?symbol=MSFT&from=2022-03-09&to=2022-03-10                         |
| Company Recommendation Trends | /company/recommendation-trends | symbol                       | https://stock-search-angular.herokuapp.com/company/recommendation-trends?symbol=MSFT                                      |
| Company Social Sentiment      | /company/social-sentiment      | symbol                       | https://stock-search-angular.herokuapp.com/company/social-sentiment?symbol=MSFT                                           |
| Company Peers                 | /company/peers                 | symbol                       | https://stock-search-angular.herokuapp.com/company/peers?symbol=MSFT                                                      |
| Company Earnings              | /company/stock/earnings        | symbol                       | https://stock-search-angular.herokuapp.com/company/stock/earnings?symbol=MSFT                                             |
