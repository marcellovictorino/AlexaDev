# AlexaDev
This is a project using Flask Framework to develop an Alexa Custom Skills

### Important Notes:
1) Flask-Ask temporarily substitute web hosting
2) In order to make it work with Alexa, necessary to use Ngrok to create available https Endpoint

obs.: every time you wish to test, necessary to repeat the following steps

## Development
### Running locally
+ a) use `ngrok` to serve a connection using localhost:5000
```bash
>> .\ngrok.exe http 5000
```
+ b) copy the last https generated url
+ c) on the [Alexa Developer Dashboard](www.developer.amazon/alexa), under Endpoint:
    - Select HTTP
    - paste generated url from Ngrok
    - SSL certification: select "Sub-domain with wild card authehtication"

> **Note**: Once Flask-ask stops running, the custom skill will no longer be available!

### Web Hosting
Using [Python Anywhere](https://www.pythonanywhere.com/), a free web-hosting service.

## To Do
Once development is complete, consider deploy using AWS lambda:
* Using Zappa as compiler
* Uploading a zip folder with all files and dependencies
