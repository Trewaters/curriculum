# Security

### Projected Time
90-180 minutes

### Prerequisites
How the Internet Works Topic Outline

### Motivation
Apprentices will learn secure development basics, common pitfalls, and how to avoid them.

### Objectives
**Participants will be able to:**
- Pull a relevant JS library up to handle common scenarios
- Validate user input
- Authenticate users on a site
- XSS someone else's web page

### Specific Things To Teach
- OWASP Secure coding practices
	- Input validation
	- Authentication means and pitfalls
	- Session management
	- Cross-site scripting (XSS)
	- Cross-site request forgery (CSRF)

### Materials

- [OWASP Secure Coding Practices Quick Reference Guide](https://www.owasp.org/images/0/08/OWASP_SCP_Quick_Reference_Guide_v2.pdf)
- [Parsley, the ultimate JavaScript form validation library](http://parsleyjs.org/)
- [Validator](https://github.com/chriso/validator.js)
- [DOMPurify](https://github.com/cure53/DOMPurify)
- [Passport](http://passportjs.org/)
- [OpenID client connect](https://github.com/IdentityModel/oidc-client-js)
- [A quick introduction to web security](https://medium.freecodecamp.org/a-quick-introduction-to-web-security-f90beaf4dd41)

### Common Mistakes / Misconceptions

OWASP releases a regular list of the [top 10 most critical web application security risks](https://www.owasp.org/index.php/Category:OWASP_Top_Ten_Project). Here are the 2017 highlights:
- Injection: validate everything before you give it to an interpreter! Here we focus on Javascript sanitization.
- Broken Authentication and Session Management: practice this by using the above libraries. Better than passwords, try SAML.
- XSS and CRSF: XSS is basically injection in the DOM, and you can't prevent CRSF until you've tackled all the XSS bugs. Try it at home with [Google](https://xss-game.appspot.com/) and [Excess XSS](http://excess-xss.com/).
- Encryption: sensitive data should be encrypted in transit and at rest. Also, you are not a mathematician; never try to roll your own encryption.

### Guided Practice

- Apprentice will use popular libraries to add authentication and session management to the Pinterest clone project. Perhaps using Google or [OpenID](http://docs.identityserver.io/en/release/quickstarts/7_javascript_client.html#refjavascriptquickstart) for SAML auth is better than trying Passport.
- Next, you can validate user input with Parsley and validate fields with Validator.
- Use DOMPurify to prevent XSS.

### Independent Practice

Build a page template to make it easier to prevent CSRF.

### Challenge

If you are feeling inclined, or interested in red teaming, you can experiment with [Insecure Labs](www.insecurelabs.org) or a [Kali Linux](https://www.kali.org/) VM and read about its rich FOSS tool suite.

### Check for Understanding

The next step is to try to XSS each other's sites.
