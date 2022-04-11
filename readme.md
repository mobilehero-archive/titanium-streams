[//]: # (header-start)

<h1 align="center">
	<a href="https://blog.axway.com/mobile-apps/changes-to-application-development-services">
		Preparing for end of Axway
	</a>	
</h1>
<h2 align="center">
	👇 &nbsp; support for Amplify Cloud and Mobile   &nbsp; 👇
</h2>	

<a href="https://brenton.house/saying-goodbye-to-axway-amplify-titanium-31a44f3671de">
	<p align="center">
		<img src="https://cdn.secure-api.org/images/RIP-Axway-Amplify-Titanium.png" alt="RIP Axway Amplify Titanium (2010 - 2022)" width="80%" />
	</p>
</a>	
<p align="center">
	<a href="https://blog.axway.com/mobile-apps/changes-to-application-development-services">
			🪦 &nbsp; RIP Axway Amplify Titanium (2010 - 2022)
	</a>
</p>
<p align="center">
	<a href="https://blog.axway.com/mobile-apps/prepare-your-apps-for-appcelerator-end-of-support">
			🪦 &nbsp; RIP Axway Amplify Cloud Services (2012 - 2022)
	</a>
</p>
<p align="center">
	<a href="https://blog.axway.com/mobile-apps/prepare-your-apps-for-appcelerator-end-of-support">
			🪦 &nbsp; RIP Axway Amplify Crash Analytics (2015 - 2022)
	</a>
</p>

<hr>
<h4 align="center">
🛑 &nbsp;&nbsp; <a href="https://blog.axway.com/mobile-apps/prepare-your-apps-for-appcelerator-end-of-support">Axway support for Amplify products has ended</a> for most products related to mobile and cloud. 
</h4>

<h4 align="center">
A few of the open-source versions of Axway Amplify products will live on after <a href="">Axway Amplify End-of-Life</a> (EOL) announcements.  However, all closed-source projects and most open-source projects are now dead.  
	</h4>

<p>&nbsp;</p>

> 👉 &nbsp;&nbsp; A group of Axway employees, ex-Axway employees, and some developers from Titanium community have created a legal org and now officially decide all matters related to future of these products.  

<p>&nbsp;</p>
<hr>


## API FAQ:

* [API Best Practices](https://brenton.house)
* [What is API Security?](https://brenton.house/what-is-api-security-5ca8117d4911)
* [OWASP Top 10 List for API Security](https://www.youtube.com/watch?v=GLVHDj0Cpg4)
* [What is API Security?](https://brenton.house/what-is-api-security-5ca8117d4911)
* [Top API Trends for 2022](https://brenton.house/top-10-api-integration-trends-for-2022-49b05f2ef299)
* [What is a Frankenstein API?](https://brenton.house/what-is-a-frankenstein-api-4d6e59fca6)
* [What is a Zombie API?](https://brenton.house/what-is-a-zombie-api-6e5427c39b6a)
* [API Developer Experience](https://brenton.house/keys-to-winning-with-an-awesome-api-developer-experience-62dd2fa668f4)
* [API Cybersecurity 101](https://brenton.house/what-is-api-security-5ca8117d4911)
* [YouTube API Videos](https://youtube.com/brentonhouse)
* [YouTube API Shorts Videos](https://youtube.com/apishorts)

&nbsp;

[![Click to watch on Youtube](https://img.youtube.com/vi/GLVHDj0Cpg4/0.jpg)](https://www.youtube.com/watch?v=GLVHDj0Cpg4&list=PLsy9MwYlG1pew6sktCAIFD5tbrXy9HUQ7  "Click to watch on YouTube")


> &nbsp; [↑ Watch video on YouTube ↑](https://www.youtube.com/watch?v=GLVHDj0Cpg4&list=PLsy9MwYlG1pew6sktCAIFD5tbrXy9HUQ7)

&nbsp;



<p>&nbsp;</p>
<hr>

<p>&nbsp;</p>
<p>&nbsp;</p>

[//]: # (header-end)


# @titanium/streams

![https://www.npmjs.com/package/@titanium/streams](https://img.shields.io/npm/v/@titanium/streams.png)

> Titanium Native mobile SDK for AMPLIFY Streams

* [📝 Description](#-description)
* [✨ Features](#-features)
* [🚀 Getting Started](#-getting-started)
	* [Installing](#installing)
	* [Connect to your API](#connect-to-your-api)
	* [Handle received data](#handle-received-data)
	* [Start receiving data](#start-receiving-data)
* [🔗 Related Links](#-related-links)
* [📚 Learn More](#-learn-more)
* [📣 Feedback](#-feedback)
* [©️ Legal](#️-legal)

## 📝 Description

AMPLIFY Streams is a real-time cache proxy allowing you to poll standard public REST APIs and push updates to clients. But wait, there is more! AMPLIFY Streams keeps an history of modifications that occur on the data between two polling! This way, AMPLIFY Streams is able to give you the list of modifications which happened since last time you fetched the data.

In other words, AMPLIFY Streams is the perfect cache to dramatically reduce the bandwidth consumption to transfer data that change both rarely and frequently.

AMPLIFY Streams Titanium SDK is based on [Axway AMPLIFY Streams JavaScript SDK](https://github.com/brentonhouse/axway-amplify-streams-js-sdk)

## ✨ Features

* [x] Incremental data update: replacing polling by push is not enough to minimize data streams. That's why streamdata.io pushes only the part that has changed.
* [x] <a href="http://www.w3.org/TR/eventsource/" target="_blank">Server-Sent-Events (SSE)</a>: updates are pushed to the client using SSE protocol. By providing fallback mechanisms streamdata.io can also work with older browsers.
* [x] API Cache: to reduce server load and latency, streamdata.io has an integrated cache mechanism.


## 🚀 Getting Started

### Installing

> Please ensure there is a package.json file in the target directory.  If there is not one present, you can create one with `npm init`.


If you wish to install this in an app using Titanium Turbo, you can execute this in the project root directory:

```
npm install @titanium/streams
```

If you wish to install this in an app using Titanium Alloy, you can execute the following in the project root directory:

```

cd app
npm install @titanium/streams

```

### Connect to your API

Create a ```StreamDataEventSource``` object into your JavaScript code.

```javascript
    var myEventSource = streamdataio.createEventSource("http://mysite.com/myRestService", <app_token>);
```

The ```StreamDataEventSource``` is the entry point for establishing a data stream connection to the given URL.

It uses an application **token** to identify and authorize the stream connection to be established.

To get a valid **token**, please visit <a href="http://streamdata.io" target="_blank">streamdata.io web site</a> to register and create an application.

It uses standard HTTP Server-Sent Events to get the data you required through streamdata.io proxy.

If your API requires specific headers, simply pass them as an array on the event source creation, and streamdata.io will forward them to your Information System.

An optional ```headers``` parameter can be passed to the ```createEventSource``` method.

It must be an array with the following structure:
```
['header1: headervalue1', 'header2: headervalue2']
```

Here is an example to add a Basic authorization header to your target API call:

```javascript

    // Your api URL
    var url = 'http://mysite.com/myJsonRestService';

    // add whatever header required by your API
    var headers = ['Authorization: Basic QWxhZGRpbjpvcGVuIHNlc2FtZQ=='];

    var myEventSource = streamdataio.createEventSource(url,<app_token>, headers);
	
```


### Handle received data

Axway Streams SDK handles data from the targeted REST service as JSON objects.

When the ```StreamDataEventSource``` object is opened, the initial set of data is returned as it would be with a standard call to the service URL. This data set is called the **snapshot**. The SDK returns it through the ```onData``` callback.

The updates of this initial set will come subsequently in the <a href="http://jsonpatch.com/" target="_blank">JSON-Patch</a> format through the ```onPatch``` callback. Such a data update is called a **patch**.

You can define your callback functions as follows:

```javascript
    myEventSource.onData(function(data){
        // initialize your data with the initial snapshot
    }).onPatch(function(patch){
        // update the data with the provided patch
    }).onError(function(error){
        // do whatever you need in case of error
    }).onOpen(function(){
        // you can also add custom behavior when the stream is opened
    });
```

### Start receiving data

```javascript
    myEventSource.open();
```


## 🔗 Related Links

- [Titanium Mobile](https://www.npmjs.com/package/titanium) - Open-source tool for building powerful, cross-platform native apps with JavaScript.
- [Titanium Alloy](https://www.npmjs.com/package/alloy) - MVC framework built on top of Titanium Mobile.
- [Appcelerator](https://www.npmjs.com/package/appcelerator) - Installer for the Appcelerator Platform tool
* [Titanium Turbo](https://www.npmjs.com/package/@titanium/turbo) - Variation of **`Titanium Alloy`** that adds some enhancements and customizations for rapid development.
* [Geek Mobile Toolkit](https://www.npmjs.com/package/@geek/mobile) - Toolkit for creating, building, and managing mobile app projects.


## 📚 Learn More

- [Axway Developer Portal](https://developer.axway.com)
- [Axway Developer Blog](https://devblog.axway.com)

## 📣 Feedback

Have an idea or a comment?  [Join in the conversation here](https://github.com/brentonhouse/titanium-eventsource)! 

## ©️ Legal

Alloy is developed by Appcelerator and the community and is Copyright © 2012-Present by Appcelerator, Inc. All Rights Reserved.

Alloy is made available under the Apache Public License, version 2. See their license file for more information.

Appcelerator is a registered trademark of Appcelerator, Inc. Titanium is a registered trademark of Appcelerator, Inc. Please see the LEGAL information about using trademarks, privacy policy, terms of usage and other legal information at http://www.appcelerator.com/legal.