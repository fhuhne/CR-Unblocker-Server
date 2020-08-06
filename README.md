# CR-Unblocker-Server

## What is the CR-Unblocker?
This is the backend we created to act a the middleman and ask a session_id for you from an american server.

## I've heard it isn't safe?
The method all Crunchyroll Unblockers are using is basically the same as described above. Your session id is bound to your account after being set as a cookie. However, I take security very serious. The server the backend is running on is secure. If you notice anything suspicious __PLEASE__ tell us.

Please note: We won't take responsibility for any compromised accounts.

## Setting it up yourself
If you are really concerned about security you can run it yourself. I will give you a brief tutorial here but can't help you with every little detail:

1. You should have some knowledge of NodeJS.
2. Clone this repo and the extension's repo.
3. Assuming you got NPM and Nodejs setup, move package.json and server.js to your VPS or something like that hosted in America. I can recommend running the server behind a reverse proxy like Nginx.
4. run `npm install`, `npm start` and setup Nginx
5. In the extension in src/background_script.js add `https://{your server URL}/start_session?version=1.0` to the `SERVERS` array and delete all other elements if you only want to use your server.
6. Add the extension folder as an unpacked extension to your browser.

## Contributing
The server and extension are currently still under development. We plan on adding some more features. If you have any idea on what to add feel free to contribute to the project.
