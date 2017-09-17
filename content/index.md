---
weight: 10
title: API Reference
---

# SMS Gateway API

Welcome to the SMS Gateway API! You can use our API to send SMS's from the device you have registered in your account.

For now we have examples in Shell but we will have more information soon. You can view code examples in the dark area to the right, and you will be able to switch the programming language of the examples with the tabs in the top right. 

# Prerequisites 

To access this API you need a API Key that you can get from the [Dashboard](http://sms-automatic-sending.appspot.com/). 

The process is the following:


1. Go to the [Dashboard](http://sms-automatic-sending.appspot.com/).
2. Access with your Gmail Account.
3. Link your device.
    1. Install the Android App from the [Play Store](https://play.google.com/store/apps/details?id=es.ngel.smssend). 
    2. Agree and start the linking process in the [Dashboard](http://sms-automatic-sending.appspot.com/).
    3. Go to your [email](http://gmail.com).
    4. Copy the code from your email.
    5. Paste the code in the app.
4. Connect your App: Your app have to be OPEN to send the sms's.
    1. Open the App.
    2. Click in the "Link" button to start sending messages.
5. Once all the previous steps are finished you can gatther the API Key from the [Dashboard](http://sms-automatic-sending.appspot.com/).
6. Consume this API.
6. Send all your SMS's!!!.º

<aside class="notice">
You must replace <code>APIKEY</code> with your personal API key.
</aside>

# Send

## Send an SMS's



```shell
curl \
    -X POST "http://sms-automatic-sending.appspot.com/api/send?apikey=APIKEY" \
    -H "Content-Type: application/json" \
    -d '
    {
    	"Number":"5555555555",
    	"Text":"Your message"
    }
    '
```

> The above command returns the following:

> Published a message; msg ID: 154147390491302


This end poing enqueue a message.

### HTTP Request

`POST http://sms-automatic-sending.appspot.com/api/send`

### Query Parameters

Parameter | Description
--------- | -----------
apikey | Your API Key from the Dashboard

<aside class="success">
Remember — You must replace APIKEY with your personal API key.
</aside>
