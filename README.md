# stackdriver-to-discord

⚙️ A simple Google Cloud Function in Go to transform / proxy Stackdriver Static Webhook notifications to Discord.

_This requires Google Cloud Functions Alpha with Go support._

![Notification in Discord](screenshot.png "Notification in Discord")


## Getting Started

1. Clone / download a copy of this repository
2. Copy `.env.sample.yaml` to `.env.yaml`, and modify the environment variables declared in the file
3. Run `./deploy.sh`
4. Configure Stackdriver static webhook notification in https://app.google.stackdriver.com/settings/accounts/notifications/static-webhook/add

_Be sure to append `?auth_token=<AUTH_TOKEN>` to the end of the URL under `httpsTrigger` (returned in the output from (3)). e.g. https://my-region-my-organisation.cloudfunctions.net/stackdriver-to-discord?auth_token=123456._
