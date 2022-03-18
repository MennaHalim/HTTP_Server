# Description:
Implementation of part of the HTTP protocol using socket programming APIs.
# Features:
 •	Threaded (multiple clients)
 •	GET method only (retrieve an HTML document).
 •	Error handling
   o	Page Not found
   o	Bad Request
   o	Redirection
   o	Internal Server Error
 •	Response Headers includes 
 •	Content-Type
 •	Length
 •	Date
 •	Location
# Responses:
 •	400 Bad Request
    I If there is any parsing error in the request.

    Validations on the request:-
      -	Check single space separating the request line parameters.
      -	Method URI HTTPVersion.
      -	Check blank line separating the header lines and the content, even if the content is empty Check valid URI.
      -	Check at least request line and host header andblank lines exist.
      
 •	301 Redirection Error
    If the URI exists in the configuration.RedirectionRules, then return 301 Redirection Error and add location header with the new redirected URI.
 •	404 Not Found error.
    If the physical file is not found.
•	500 Internal Server Error.
   If there is any unknown exception.
   
# Test cases:
Try the following URIs in the web browser:

http://localhost:1000/aboutus2.html
should display aboutus2.html page

http://localhost:1000/aboutus.html
should display aboutus2.html (redirection)

http://localhost:1000/main.html
should display main page

http://localhost:1000/blabla.html
should display 404 page.






