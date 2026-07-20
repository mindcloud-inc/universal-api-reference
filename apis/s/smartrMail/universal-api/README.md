# <img src="https://images.mindcloud.co/apps/icons/smartr-mail_1774361339833.png" alt="SmartrMail logo" width="28" height="28"> SmartrMail: Universal API

Manage subscriber lists and subscribers in SmartrMail

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/smartrMail/latest
- **Category:** Marketing
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.smartrmail.com
- **Vendor API docs:** https://docs.smartrmail.com/en/collections/30284-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Subscriber Lists](actions/list-subscriber-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartrMail/latest/actions/list-subscriber-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [Add Subscribers to List](actions/add-subscribers-to-list.md) | POST | Adds subscribers to a specific SmartrMail list. |
| [Get Subscriber](actions/get-subscriber.md) | GET | Retrieves a subscriber from SmartrMail by identifier. |
| [List Subscribers in List](actions/list-subscribers-in-list.md) | GET | Retrieves subscribers from a specific SmartrMail list. |
| [Remove Subscriber From List](actions/remove-subscriber-from-list.md) | DELETE | Removes a subscriber from a specific SmartrMail list. |
| [Resubscribe Subscriber](actions/resubscribe-subscriber.md) | PUT | Resubscribes a subscriber in SmartrMail by identifier. |
| [Unsubscribe Subscriber](actions/unsubscribe-subscriber.md) | PUT | Unsubscribes a subscriber in SmartrMail by identifier. |
| [Update Subscriber](actions/update-subscriber.md) | PUT | Updates an existing subscriber in SmartrMail. |

### Subscriber List

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscriber List](actions/create-subscriber-list.md) | POST | Creates a new subscriber list in SmartrMail. |
| [Delete Subscriber List](actions/delete-subscriber-list.md) | DELETE | Deletes an existing subscriber list from SmartrMail. |
| [Get Subscriber List](actions/get-subscriber-list.md) | GET | Retrieves a subscriber list from SmartrMail. |
| [List Subscriber Lists](actions/list-subscriber-lists.md) | GET | Retrieves subscriber lists from your SmartrMail account. |
| [Update Subscriber List](actions/update-subscriber-list.md) | PUT | Updates an existing subscriber list in SmartrMail. |

