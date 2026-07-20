# <img src="https://images.mindcloud.co/apps/icons/engage-app_1775575557859.png" alt="Engage logo" width="28" height="28"> Engage: Universal API

Engage is a customer engagement platform for managing users, lists, events, and transactional messaging across email and SMS.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/engage/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://engage.so
- **Vendor API docs:** https://docs.engage.so/en-us/a/62bbdd015bfea4dca4834041-api-overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/engage/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Batch Request

| Action | Method | Description |
| --- | --- | --- |
| [Queue Batch Request](actions/queue-batch-request.md) | POST | Queues batched user creates, updates, and events in Engage. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Send Email](actions/send-email.md) | POST | Sends a transactional email through Engage. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Track User Event](actions/track-user-event.md) | POST | Tracks a user event in Engage. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Archive List](actions/archive-list.md) | DELETE | Archives an existing list in Engage. |
| [Create List](actions/create-list.md) | POST | Creates a new list in Engage. |
| [Get List](actions/get-list.md) | GET | Retrieves a list from Engage by ID. |
| [List Lists](actions/list-lists.md) | GET | Retrieves user lists from Engage with pagination. |
| [Remove Subscriber from List](actions/remove-subscriber-from-list.md) | DELETE | Removes a subscriber from an Engage list. |
| [Subscribe User to List](actions/subscribe-user-to-list.md) | POST | Subscribes a user to a list in Engage, creating them if needed. |
| [Update List](actions/update-list.md) | PUT | Updates an existing list in Engage. |
| [Update Subscriber Status](actions/update-subscriber-status.md) | PUT | Updates a user's subscription status for an Engage list. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Send SMS](actions/send-sms.md) | POST | Sends a transactional SMS through Engage. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Add Customer to Accounts](actions/add-customer-to-accounts.md) | PUT | Adds a customer to one or more accounts in Engage. |
| [Add User to Lists](actions/add-user-to-lists.md) | PUT | Adds a user to one or more lists in Engage. |
| [Archive User](actions/archive-user.md) | DELETE | Archives a customer or account in Engage. |
| [Change Account Role](actions/change-account-role.md) | PUT | Updates a customer's role in an Engage account. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes a customer or account from Engage. |
| [List Account Members](actions/list-account-members.md) | GET | Retrieves members of an account from Engage. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Engage with optional email filtering. |
| [Merge Users](actions/merge-users.md) | PUT | Merges one user into another in Engage. |
| [Remove Customer from Account](actions/remove-customer-from-account.md) | DELETE | Removes a customer from an account in Engage. |
| [Retrieve User](actions/retrieve-user.md) | GET | Retrieves a user from Engage by user ID. |
| [Update User Attributes](actions/update-user-attributes.md) | PUT | Updates a user in Engage, or creates one if missing. |
| [Update User Type](actions/update-user-type.md) | PUT | Converts a user between customer and account in Engage. |

