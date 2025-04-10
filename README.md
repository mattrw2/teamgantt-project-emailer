# TeamGantt Project PDF Emailer

### Prerequisites
- [Node](https://nodejs.org/en/download)
- [Git](https://git-scm.com/downloads)


### Setup 

1. Clone repository
    ```
    git clone https://github.com/mattrw2/teamgantt-project-emailer.git
    ```
1. CD into the directory
    ```
    cd teamgantt-project-emailer
    ```

1. Install dependencies
    ```
    npm install && npx playwright install
    ```
1. Add a `.env` file at the root of the project. Populate with secrets. See `.env.example`

1. Populate `accounts.json` with client and project data


### Running Scripts

You must pass a `date` argument to `npm start` in order to run the script. This helps to prevent us from sending the same weekly report multiple times accidentally. It also allows us to re-run the same date if some of the emails failed to send without re-sending the previously successful emails.

- Create PDFs and save them in the "/reports" folder, but don't send them. 
    ```
    npm start -- --simulate=true --date=yyyy-mm-dd
    ```

- Create PDFs and send them to the email specified in the `accounts.json` file.
    ```
    npm start -- --date=yyyy-mm-dd
    ```
