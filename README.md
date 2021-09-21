# Google-Map-API

Simple app created by HTML, CSS, JavaScript and Maps JavaScript API.

#### _Prerequisite_ :

Before you start using the Maps JavaScript API, you need a project with a billing account and the Maps JavaScript API enabled. To learn more, see Set up in Cloud Console.

#### Doc Sources :

https://developers.google.com/maps/documentation/javascript/overview

https://developers.google.com/maps/documentation/javascript/get-api-key

## How to create a Google map's API_Key ?

Google Maps Platform products are secured from unauthorized use by restricting API calls to those that provide proper authentication credentials. These credentials are in the form of an API key - a unique alphanumeric string that associates your Google billing account with your project, and with the specific API or SDK.

This guide shows how to create, restrict, and use your API Key for Google Maps Platform.

The API key is a unique identifier that authenticates requests associated with your project for usage and billing purposes. You must have at least one API key associated with your project.

1. Go to the Google Maps Platform > Credentials page.
   https://console.cloud.google.com/projectselector2/google/maps-apis/credentials

2. On the Credentials page, click Create credentials > API key.
   The API key created dialog displays your newly created API key.

3. Click Close.
   The new API key is listed on the Credentials page under API keys.
   (Remember to restrict the API key before using it in production.)

## How to restrict your Google map's API_Key ?


Restricting API keys adds security to your application by ensuring only authorized requests are made with your API key. We strongly recommend that you follow the instructions to set restrictions for your API keys. For more information, see API security best practices.


1. Go to the Google Maps Platform > Credentials page.
   https://console.cloud.google.com/projectselector2/google/maps-apis/credentials

2. Select the API key that you want to set a restriction on. The API key property page appears.
3. Under Key restrictions, set the following restrictions:

   #### Application restrictions :

   * a. To accept requests from the list of website that you supply, select HTTP
   referrers (web sites) from the list of Application restrictions.
   * b. Specify one or more referrer web sites. For example, _.google.com accepts all
   sites ending in google.com, such as https://developers.google.com.
   Note: file:// referers need a special representation to be added to the key restriction. The "file://" part should be replaced with "**file_url**" before being added to the key restriction. For example, "file:///path/to/" should be formatted as "**file_url**//path/to/_". After enabling file:// referers, it is recommended you regularly check your usage, to make sure it matches your expectations.

   #### API restrictions :

   * a. Click Restrict key
   * b. Select Maps JavaScript API from Select APIs dropdown. If the Maps JavaScript API is  
    not listed, you need to enable it.
   *c. If your project uses Places Library, also select Places API. Similarly, if your
   project uses other services in the JavaScript API (Directions Service, Distance Matrix Service, Elevation Service, and/or Geocoding Service), you must also enable and select the corresponding API in this list.

4. To finalize your changes, click Save.
