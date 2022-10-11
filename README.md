# PRO-C178-Boilerplate
# 178

Maps are basically a 2D representation drawn to scale any 3D spaces around us.


first Map was drawn around 5000 years ago!

When humans were evolving but still living in the cave, they learned the art to write and draw. They used symbols
to draw something related to their religious beliefs.
But recent findings tell that some of these paintings were maps of huntings ,or routes of traveling, or even
maps of stars.

we can imagine humans have been making maps since long ago.
--------------------------------------------------------------------------------------------------------------------
 the art of making maps is called Cartography
 
 Cartographers study and design maps on the basis of geographical areas.
 
people across the world started traveling a lot to discover new things.
Along with this they also discovered new places and started making maps.
And slowly the complete world was drawn on the paper.

First world map was drawn around 1500 years ago!
--------------------------------------------------------------------------------------------------------------------
Now everyone is using the most popular digital maps application, Google Maps!

It has made our lives so convenient, whenever we want to find places!
Not only finding places but also navigating from one place to another.
Today we will be learning how we use digital maps in our web application.
-------------------------------------------------------------------------------------------------------------------
main.html: The HTML content file
● main.css: Styling file
● main.js: JavaScript file
-------------------------------------------------------------------------------------------------------------------
Once we have the HTML content structure of the page ready, let’s see how we can render maps on the web
page. For this we are going to use Mapbox GL JS library.

Mapbox GL JS is a JavaScript library that is designed to render interactive maps in the web application. This library uses WebGL API in the background.

WebGL stands for Web Graphics Library.

Graphics are pictures and drawings used to represent something.
Graphics are a pictorial representation of any object.
Pictures help us understand better rather than just explaining in words.

Maps are a good example of graphics.You can easily understand the way from one place to another by looking at
a map, instead of someone explaining the way.

WebGL is a JavaScript API which helps us to render 2D and 3D graphics
------------------------------------------------------------------------------------
A-Fame is built using Three.js library which uses WebGL behind the scenes
to render 3D objects. Now since we want to use Mapboxlibrary APIs,

we should include these in the <head> tag.
<script src='https://api.mapbox.com/mapbox-gl-js/v2.2.0/mapbox-gl.js'></script>

 Mapbox also provides their own CSS to use for the maps.We will need to include that also in the
<head> tag.
<link href='https://api.mapbox.com/mapboxgl-js/v2.2.0/mapbox-gl.css' rel='stylesheet' />


-----------------------------------------------------------------------------------
 
 Now to access the properties and methods of these APIs we will need an access token.

Access tokens are a way to know which user is accessing the APIs.
Access tokens are entry points to call any of the APIs that we want to use.
To get the access token, we will have to first create a Mapbox account.
 
 create a mapbox account
 https://account.mapbox.com/auth/signin/?route-to=%22https://account.mapbox.com/%22
 
 steps to create a/c:
 https://obj.whitehatjr.com/b16395ba-85d6-40ec-8d46-44c27a20a27a.pdf
 
We will use the “Default public token”” to access the API.
We are going to use the mapboxgl global variable to use the accessToken property
 
copy the “Default public token” from the Mapbox account dashboard and assigns it to mapboxgl.accessToken property in main.js file.


----------------------------------------------------------------------------------------

Test the output with zoom level 0. We should be able to see the whole world map.

To add controls in the Mapbox maps, the Map class provides a method called addControl(control, position).

There a few predefined controls available in the Mapbox, like:
 
● GeolocateControl: This control provides the button that will use the browser's location to find the current location of the user.
 
● NavigationControl: This control contains the zoom in and zoomout buttons.
 
● position: position of the control on the page.
 
● valid values: 'top-left' , 'top-right' , 'bottom-left' , andbottom-right'. Default: 'top-right'.
 
---------------------------------------------------------------------------------------------------------
 
 The GeolocateControl can also have many options inside it. But we are going to use:

 positionOptions:
default:
{
enableHighAccuracy:false,
timeout:6000
}
 
trackUserLocation: default: false
