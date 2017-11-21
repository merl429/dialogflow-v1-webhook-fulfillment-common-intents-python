# Dialogflow v1 (previously Api.ai) - webhook implementation for common tools in Python

This is a really simple webhook implementation that gets Dialogflow classification JSON (i.e. a JSON output of Dialogflow /query endpoint) and returns a fulfillment response.

More info about Dialogflow webhooks could be found here:
[Dialogflow Webhook](https://dialogflow.com/docs/fulfillment)

# Deploy to:
[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

# What does the service do?

This provides fulfillment for the following intents:
  1. Weather - uses [Yahoo! Weather API](https://developer.yahoo.com/weather/)
    Action: yahooWeatherForecast
    Parameters:
      geo-city
    
  2. Currency Converter - uses [Currencyfeed data sheet API](http://currencyfeed.com/)
    Action: currencyFeedConverter
    Parameters:
      Currency (String, Currency to convert to, 3 character currency code)
      unit-currency (Object)
        currency (Base currency to convert from, 3 character currency code)
        amount (amount of base currency to convert)

The service packs the result in the Dialogflow webhook-compatible response JSON and returns it to Dialogflow.

## How to make contributions?
Please read and follow the steps in the [CONTRIBUTING.md](CONTRIBUTING.md).

## License
See [LICENSE](LICENSE).

## Terms
Your use of this sample is subject to, and by using or downloading the sample files you agree to comply with, the [Google APIs Terms of Service](https://developers.google.com/terms/).

This is not an official Google product
