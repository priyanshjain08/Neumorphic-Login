Neumorphic Login & Welcome Page
A simple, responsive login and account-creation interface built with HTML, CSS, and JavaScript. The project uses a neumorphic design, animated input highlights, a flip transition between login and sign-up forms, and a separate welcome page.
Features
Neumorphic UI: Soft shadows, rounded cards, and a light background.
Login form: Email and password fields.
Show/hide password: Toggle password visibility in the login and sign-up forms.
Remember me and forgot password: UI elements are included on the login screen.
Create account screen: Flip animation switches between login and sign-up forms.
Input focus effect: Animated gradient outline appears when an input is focused.
Welcome page: A separate page is shown when the configured demo credentials match.
Responsive layout: The card adapts to smaller viewport widths.
Google Fonts: Uses the Poppins font from Google Fonts.
Project structure
```text
project/
├── login.html
├── welcome.html
└── README.md
```
Keep `login.html` and `welcome.html` in the same folder unless you update the redirect path in `login.html`.
Run locally
Download or clone the project files.
Make sure `login.html` and `welcome.html` are in the same directory.
Open `login.html` in a modern web browser.
Enter the demo credentials configured in the JavaScript section of `login.html`.
If the credentials match, the browser redirects to `welcome.html`.
No package manager, build step, or local server is required for this basic static demo. An internet connection is needed to load the Poppins font from Google Fonts; otherwise, the fallback system font is used.
Configure the demo login
Near the bottom of `login.html`, find:
```javascript
const ALLOWED_EMAIL = 'your-email@example.com';
const ALLOWED_PASSWORD = 'your-password';
```
Replace the example values with the values you want to use for your local demo. The actual file currently contains hard-coded credentials, so avoid sharing that file publicly with real credentials.
The redirect is set to:
```javascript
window.location.href = 'welcome.html';
```
Change the path if you rename or move the welcome page.
Important limitations
This is a front-end demonstration, not a complete authentication system.
The allowed email and password are stored in client-side JavaScript and can be viewed by anyone who can access the source.
There is no server-side authentication, database, account creation endpoint, or password storage system.
The sign-up form is currently a visual interface; it does not create or save an account.
“Remember me” and “Forgot Password?” are displayed as UI elements but do not implement persistence or password recovery.
The “GET STARTED” button on the welcome page does not currently perform an action.
The login form uses custom JavaScript credential comparison rather than a production authentication flow.
For production use: implement authentication on a secure backend, store password hashes rather than plaintext passwords, use HTTPS, validate inputs on the server, and provide proper account recovery and session management. Never rely on client-side checks to protect private pages.
Technologies
HTML5
CSS3 (animations, transforms, custom properties, neumorphic shadows)
Vanilla JavaScript
Google Fonts — Poppins
License
No license is specified in the provided files. Add a `LICENSE` file if you plan to distribute the project and want to define reuse terms.
