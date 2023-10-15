# Simple Scrapy Spider for MindBodyOnline

Using a basic Spider and the MindBodyOnline I was able to scrape data for gyms all over the USA. The site is rendered in Javascript and Uses an API to get the data. I was able to use that API to scrape the data.

## API

Request URL = https://prod-mkt-gateway.mindbody.io/v1/search/locations

Example Payload: '''{
                              "sort":"-_score,distance",
                              "page":{"size":50,"number":1},
                              "filter":{"categories":"any",
                                        "latitude":40.712775,
                                        "longitude":-74.0059721,
                                        "categoryTypes":"any"}
                       }'''

The payload is used in the Request body. Only the page number, latitude and longitude change for each request. I downloaded a csv file of cities in the USA which included lat / long values. 

The Insomnia desktop app was used to get the request headers.

## Usage

This was implemented as a simple py file that can be run directly. I wanted to see if I could write a simple script and avoid the overhead of a full Scrapy project. This project was completed as a learning project. Learning how to use the API was a great help!
