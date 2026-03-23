# EDA-AutoSync

Steps:

1. In SyncProjects.yml, change "project:" names in the conditional statements to the names of your Github Repos. Add additional conditional statements if more projects are present
2. In SyncProjects.yml, change "repository_name" variables to the name of your projects inside of AAP
3. Create a EDA credential of type "Github Event Stream" and place your HMAC token from Github in the credential
4. Create an Event stream in EDA with the "Github Event Stream" type and place your credential created in step 3 in the "credential" field
5. In your Github Repos, create webhooks, and set the Payload URL to the event stream URL given by your newly created event stream
6. Create a rulebook activation in EDA and link it to Sync_Webhook_Injest.yml
7. Create a template in Automation controller and link it to SyncPropjects.yml
8. Test your new automation by making a change to your Github Repo

