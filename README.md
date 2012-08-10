wsse.js - Generate WSSE authentication header in JavaScript
(C) 2005 Victor R. Ruiz <rvr*linotipo.es> - http://rvr.typepad.com/

Parts:
* SHA-1 library (C) 2000-2002 Paul Johnston - BSD license
* ISO 8601 function (C) 2000 JF Walker All Rights
* Base64 function (C) aardwulf systems - Creative Commons

The current default authentication method in TypePad and Movable Type's Atom implementation is WSSE. WSSE is a header containing a token based on username, password and date and looks like:

X-WSSE: UsernameToken Username="name", PasswordDigest="digest", Created="timestamp", Nonce="nonce"

I have implented a library in JavaScript to generate this header, quite useful for XmlHttpRequest and GM\_XmlHttpRequest functions. An example of use:

'''javascript
<html>
<head>
  <script language="JavaScript1.2" src="wsse.js">
</head>
<body>
<script language="JavaScript1.2">
   var w = wsseHeader(Username, Password);
   alert('X-WSSE: ' + w);
</script>
</body>
'''

This library uses code from Paul Johnston,  JF Walker and aardwulf systems.
