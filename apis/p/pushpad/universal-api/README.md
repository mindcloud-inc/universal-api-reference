# <img src="https://images.mindcloud.co/apps/icons/pushpad_1775138646773.png" alt="Pushpad logo" width="28" height="28"> Pushpad: Universal API

Send push notifications and manage projects, senders, and subscriptions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pushpad/latest
- **Category:** Marketing
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pushpad.xyz
- **Vendor API docs:** https://pushpad.xyz/docs/rest_api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushpad/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Scheduled Notification](actions/cancel-scheduled-notification.md) | DELETE | Cancels a scheduled notification in Pushpad. |
| [Get Notification](actions/get-notification.md) | GET | Retrieves a Pushpad notification and its stats. |
| [List Latest Notifications](actions/list-latest-notifications.md) | GET | Retrieves the latest notifications from a Pushpad project. |
| [Send Notification](actions/send-notification.md) | POST | Sends a web push notification with Pushpad. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Pushpad. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Pushpad asynchronously. |
| [Get Project](actions/get-project.md) | GET | Retrieves a specific project from Pushpad. |
| [List Projects](actions/list-projects.md) | GET | Retrieves all projects available in Pushpad. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Pushpad. |

### Sender

| Action | Method | Description |
| --- | --- | --- |
| [Create Sender](actions/create-sender.md) | POST | Creates a new sender in Pushpad. |
| [Delete Sender](actions/delete-sender.md) | DELETE | Deletes an existing sender from Pushpad. |
| [Get Sender](actions/get-sender.md) | GET | Retrieves a specific sender from Pushpad. |
| [List Senders](actions/list-senders.md) | GET | Retrieves all senders available in Pushpad. |
| [Update Sender](actions/update-sender.md) | PUT | Updates an existing sender in Pushpad. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Create or Import Subscription](actions/create-or-import-subscription.md) | POST | Creates or imports a subscription into a Pushpad project. |
| [Delete Subscription](actions/delete-subscription.md) | DELETE | Deletes a subscription from a Pushpad project. |
| [Get Subscription](actions/get-subscription.md) | GET | Retrieves a subscription from a Pushpad project. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from a Pushpad project. |
| [Update Subscription](actions/update-subscription.md) | PUT | Updates a subscription in a Pushpad project. |

