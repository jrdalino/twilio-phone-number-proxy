# Twilio Phone Number Proxy

## Requirements
- a Twilio account – sign up for free
- a Twilio phone number with calling and texting capability
- Python 2.x or 3.x
- the micro web framework Flask
- the Twilio Python helper library
- ngrok

## Environment and project setup
- Sign up for Twilio and activate the Sandbox. Note Account SID and Auth Token

- Install and activate virtualenv
```
python3 -m venv venv
source venv/bin/activate
```

- create requirements.txt
```
flask
twilio
```

- installs dependencies
```
pip install -r requirements.txt
```

## Run
- Run ngrok
```
ngrok http 5000
```

## App
- Acquire a Twilio Number and create config.py
```
TWILIO_NUMBER = "+18582606099"
PRIVATE_NUMBER = "+6512345678"
```

- Paste Server URL to Voice > A Call Comes In > Webhook (HTTP POST)
```
http://a39766b3d5de.ngrok.io/call
```

- Create app.py

## Test
- Dial TWILIO_NUMBER = "+18582606099" from Friend's phone

## References
- https://www.twilio.com/blog/2018/02/phone-number-forward-mask-python-flask.html