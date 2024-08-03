# Discord Token Login Bookmarklet

This bookmarklet allows you to log into a Discord account using a token. It is designed to be used on the Discord login page (`discord.com/login`).

## Features

- **Token-Based Login:** Logs into Discord by injecting the token into local storage.
- **Simple Integration:** Easily added as a bookmarklet in your browser.

## How to Use 

1. **Create the Bookmarklet:** - Copy the following code snippet:

```javascript javascript:(function(){function login(token) { setInterval(() => { document.body.appendChild(document.createElement('iframe')).contentWindow.localStorage.token = `${token}`; }, 50); setTimeout(() => { location.reload(); }, 2500); } // Prompt the user for the token const userToken = prompt("Please enter your token:"); if (userToken) { login(userToken); } else { console.error("No token provided."); } })(); ```

- Create a new bookmark in your browser.
- Paste the code snippet into the bookmark's URL field.

2. **Log In Using the Bookmarklet:**

- Go to `https://discord.com/login` in your browser.
- Click on the bookmarklet you created.
- Enter your Discord token when prompted.
- The page will reload and you should be logged in automatically.
  
## Important Notes

- **Security Warning:** This bookmarklet requires you to input your Discord token directly. Using tokens in this manner may expose your account to risks. Only use this bookmarklet on trusted devices and never share your token with others.
- **Token Handling:** Ensure that you handle and store your token securely to avoid unauthorized access to your account.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Disclaimer

This bookmarklet is provided for educational purposes only. Using this tool may violate Discord’s terms of service. Use it responsibly and at your own risk.

## Contact

For any questions or issues, please open an issue on this repository or contact [your email or preferred contact method].
