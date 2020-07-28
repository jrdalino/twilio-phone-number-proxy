# Twilio Phone Number Proxy

## Requirements
- a Twilio account – sign up for free
- a Twilio phone number with calling and texting capability
- Python 2.x or 3.x
- the micro web framework Flask
- the Twilio Python helper library
- ngrok

## Local Development
- Activate Virtual Env: source venv/bin/activate and Run App
```
$ python3 -m venv venv
$ source venv/bin/activate
```

- create requirements.txt
```
flask
twilio
```

- installs dependencies
```
$ pip install -r requirements.txt
```

- Acquire a Twilio Number and create config.py
```
TWILIO_NUMBER = "+18582606099"
PRIVATE_NUMBER = "+65REPLACE_ME" >> DANGER: DO NOT PUSH ME TO GIT!
```

- Work on app.py

## Usage / Demo
- Step 1: Go to https://github.com/jrdalino/twilio-phone-number-proxy

- Step 2:  Activate Virtual Env: source venv/bin/activate and Run App
```
$ python3 -m venv venv
$ source venv/bin/activate
```

- Step 3: Run ngrok to  allow us to expose your localhost at port 5000 to incoming requests. We will be using this to allow Twilio to communicate with our local python server.
```
$ ngrok http 5000
```

- Step 4: Paste Server URL to Voice > A Call Comes In > Webhook (HTTP POST)
```
https://www.twilio.com/console/phone-numbers/PN73ff9e69b7ca2979fd0e4c2d29ac3b96
http://95775f3dc1d1.ngrok.io/call
```

- Step 5: Run your app
```
$ python3 app.py 
```

- Step 6: Dial TWILIO_NUMBER = "+18582606099" from Driver's phone

## References
- https://www.twilio.com/blog/2018/02/phone-number-forward-mask-python-flask.html