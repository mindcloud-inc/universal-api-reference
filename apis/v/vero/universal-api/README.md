# <img src="https://images.mindcloud.co/apps/icons/2190469_1774377149706.png" alt="Vero logo" width="28" height="28"> Vero: Universal API

Vero is a customer messaging and event tracking platform for lifecycle messaging and product data ingestion.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vero/latest
- **Category:** Marketing
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.getvero.com/
- **Vendor API docs:** https://help.getvero.com/api-reference/track/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Trigger](actions/get-trigger.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vero/latest/actions/get-trigger?connectionId=$CONNECTION_ID&id=trigger_example" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Campaign](actions/cancel-campaign.md) | DELETE | Cancels an existing campaign in Vero. |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a new campaign in Vero. |
| [Launch Campaign](actions/launch-campaign.md) | PUT | Launches an existing campaign in Vero. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves all campaign records from Vero. |
| [Retrieve Campaign](actions/retrieve-campaign.md) | GET | Retrieves a campaign record from Vero. |
| [Update Campaign](actions/update-campaign.md) | PUT | Updates an existing campaign in Vero. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Track Event](actions/track-event.md) | POST | Tracks an event record in Vero. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [List Messages](actions/list-messages.md) | GET | Retrieves all message records from Vero. |
| [Retrieve Message](actions/retrieve-message.md) | GET | Retrieves a message record from Vero. |
| [Update Message](actions/update-message.md) | PUT | Updates an existing message in Vero. |

### Trigger

| Action | Method | Description |
| --- | --- | --- |
| [Get Trigger](actions/get-trigger.md) | GET | Retrieves a trigger record from Vero. |
| [Update Trigger](actions/update-trigger.md) | PUT | Updates an existing trigger in Vero. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Alias](actions/alias.md) | PUT | Aliases an existing user record in Vero. |
| [Delete User](actions/delete-user.md) | DELETE | Deletes an existing user from Vero. |
| [Edit Tags](actions/edit-tags.md) | PUT | Updates a user's tags in Vero. |
| [Identify](actions/identify.md) | POST | Identifies a user profile in Vero. |
| [Resubscribe](actions/resubscribe.md) | PUT | Resubscribes a user in Vero globally. |
| [Unsubscribe](actions/unsubscribe.md) | PUT | Unsubscribes a user in Vero globally. |

