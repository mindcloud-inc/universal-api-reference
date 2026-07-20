# <img src="https://images.mindcloud.co/apps/icons/userflow-icon-filled-256_1774025588705.png" alt="Userflow logo" width="28" height="28"> Userflow: Universal API

Userflow lets you sync users, groups, and events into Userflow to personalize in-app onboarding and product adoption flows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/userflow/latest
- **Category:** Support / Customer Success
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://userflow.com
- **Vendor API docs:** https://docs.userflow.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userflow/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Actions

| Action | Method | Description |
| --- | --- | --- |
| [Get Content](actions/get-content.md) | GET | Retrieves a content object from Userflow by ID. |
| [List Content](actions/list-content.md) | GET | Retrieves a list of content objects from Userflow. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [List Attribute Definitions](actions/list-attribute-definitions.md) | GET | Retrieves a list of attribute definitions from Userflow. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Track Event](actions/track-event.md) | POST | Tracks a user or group event in Userflow. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [List Event Definitions](actions/list-event-definitions.md) | GET | Retrieves a list of event definitions from Userflow. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Group](actions/create-or-update-group.md) | POST | Creates or updates a group in Userflow. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from Userflow. |
| [List Groups](actions/list-groups.md) | GET | Retrieves a list of groups from Userflow. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update User](actions/create-or-update-user.md) | POST | Creates or updates a user in Userflow. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes an existing user from Userflow. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Userflow by ID. |
| [List Users](actions/list-users.md) | GET | Retrieves a list of users from Userflow. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | POST | Creates a webhook subscription in Userflow. |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | DELETE | Deletes an existing webhook subscription from Userflow. |
| [Get Webhook Subscription](actions/get-webhook-subscription.md) | GET | Retrieves a webhook subscription from Userflow by ID. |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | GET | Retrieves a list of webhook subscriptions from Userflow. |
| [Update Webhook Subscription](actions/update-webhook-subscription.md) | PUT | Updates an existing webhook subscription in Userflow. |

