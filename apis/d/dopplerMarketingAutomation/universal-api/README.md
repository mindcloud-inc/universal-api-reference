# <img src="https://images.mindcloud.co/apps/icons/doppler_1776187241195.jpeg" alt="Doppler Marketing Automation logo" width="28" height="28"> Doppler Marketing Automation: Universal API

Doppler Marketing Automation connects to Doppler's REST API for email marketing account resources such as lists, subscribers, fields, tasks, and unsubscribed contacts.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dopplerMarketingAutomation/latest
- **Category:** Marketing
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.fromdoppler.com
- **Vendor API docs:** https://restapi.fromdoppler.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Lists](actions/list-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Account Home

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Home](actions/get-account-home.md) | GET | Retrieves account details from Doppler Marketing Automation. |

### Api Index

| Action | Method | Description |
| --- | --- | --- |
| [Get API Index](actions/get-api-index.md) | GET | Retrieves the Doppler API index. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Associate Subscriber](actions/associate-subscriber.md) | POST | Creates a subscriber association in Doppler Marketing Automation. |
| [Get Subscriber](actions/get-subscriber.md) | GET | Retrieves a subscriber from Doppler Marketing Automation. |
| [List Subscribers](actions/list-subscribers.md) | GET | Retrieves subscribers from a Doppler Marketing Automation list. |
| [List Unsubscribed Subscribers](actions/list-unsubscribed-subscribers.md) | GET | Retrieves unsubscribed subscribers from Doppler Marketing Automation. |
| [Unsubscribe Subscriber](actions/unsubscribe-subscriber.md) | PUT | Updates a subscriber to unsubscribed in Doppler Marketing Automation. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [List Fields](actions/list-fields.md) | GET | Retrieves fields from Doppler Marketing Automation. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST | Creates a new list in Doppler Marketing Automation. |
| [Delete List](actions/delete-list.md) | DELETE | Deletes an existing list from Doppler Marketing Automation. |
| [Get List](actions/get-list.md) | GET | Retrieves a list from Doppler Marketing Automation. |
| [List Lists](actions/list-lists.md) | GET | Retrieves lists from Doppler Marketing Automation. |
| [Update List](actions/update-list.md) | PUT | Updates an existing list in Doppler Marketing Automation. |

### Subscriber Import

| Action | Method | Description |
| --- | --- | --- |
| [Import Subscribers](actions/import-subscribers.md) | POST | Creates a subscriber import job in Doppler Marketing Automation. |
| [Import Subscribers To List](actions/import-subscribers-to-list.md) | POST | Creates a subscriber import job in Doppler Marketing Automation. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Doppler Marketing Automation. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Doppler Marketing Automation. |

### Unsubscribed Import

| Action | Method | Description |
| --- | --- | --- |
| [Import Unsubscribed Subscribers](actions/import-unsubscribed-subscribers.md) | POST | Creates an unsubscribed import job in Doppler Marketing Automation. |

