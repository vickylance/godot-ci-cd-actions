# godot-ci-cd-actions
A example of how to setup Godot CI/CD and auto publish to Itch.io

## Installation and Usage

1. First create a folder `.github` in your godot project's root directory.
2. Copy the `integrate.yml` file in this repo into that directory
3. Then push the code to Github.
4. Now create a game page in itch.io
5. Now add the Game name as ITCH_GAME and your itch username as ITCH_USERNAME in the Github repo's project secrets.
You can access the Secrets by clicking on the `Settings` tab in your repo. And then clicking on `Secrets` in left panel.
And then clicking on `New Secret` and give the name as `ITCH_GAME` and give your itch game name. And click on `Add Secret`.
Similarly add for `ITCH_USERNAME` your itch username.
6. Similarly you would also have to add `BUTLER_CREDENTIALS` which you can get by following this docs (Itch Butler Key)[https://itch.io/docs/butler/login.html#running-butler-from-ci-builds-travis-ci-gitlab-ci-etc]
7. Once you add these the next time you push to master Github Actions will automatically pull in latest Godot and build for 4 platforms (Windows, MacOS, Linux and Html5)
And publish to Itch.io (Make sure you set the itch.io game page as HTML5 for html5 to work).
