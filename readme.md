JavaScript Cookie Template
This simple HTML template demonstrates how to work with cookies in JavaScript. Cookies are a type of key-value pair that can be stored on a user's browser, allowing information to persist across multiple page loads.

The template includes two JavaScript functions that allow you to set and retrieve cookies:

setCookie(cname, cvalue, exdays)
The setCookie function creates a new cookie with a specified name (cname), value (cvalue), and number of days until it expires (exdays).

The expiration date is calculated by adding the number of days specified in exdays to the current date and time. This value is then stored in a string in the format "expires=UTC_DATE", where "UTC_DATE" is the expiration date in the UTC timezone.

Finally, the document.cookie property is set to the string cname=cvalue;expires=UTC_DATE;path=/, which creates the new cookie. The path=/ component sets the path of the cookie to the root directory, allowing it to be accessible from any page on the website.

getCookie(cname)
The getCookie function retrieves the value of a cookie with a specified name (cname). It does this by splitting the value of the document.cookie property into an array of individual cookies, each separated by a semicolon.

For each cookie in the array, the function checks if the cookie's name starts with the specified cname. If it does, the function returns the part of the cookie's value that comes after cname=.

If no cookie with the specified name is found, the function returns an empty string.

Using the Template
To use the template, simply add your own HTML content to the <body> tag. You can then call the setCookie and getCookie functions as needed to store and retrieve cookies.

For example, you might use the following code to store a cookie with the name "username" and the value "john_doe":
  
  
  -----------------------------------------------------
  
  python
--Copy code--
setCookie("username", "john_doe", 365);
And then retrieve the value of the cookie using the following code:

javascript
--Copy code--
var username = getCookie("username");
