# <img src="https://images.mindcloud.co/apps/icons/images-8_1774906229722.png" alt="Postalytics logo" width="28" height="28"> Postalytics: Universal API

Create, send, and track automated direct mail campaigns

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/postalytics/latest
- **Category:** Marketing
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.postalytics.com
- **Vendor API docs:** https://docs.postalytics.com/references/postalytics-rest-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My Account](actions/get-my-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postalytics/latest/actions/get-my-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get My Account](actions/get-my-account.md) | GET | Retrieves your authenticated Postalytics account details. |

### Suppression List

| Action | Method | Description |
| --- | --- | --- |
| [Create Suppression List](actions/create-suppression-list.md) | POST | Creates a suppression list in Postalytics. |
| [Delete Suppression List](actions/delete-suppression-list.md) | DELETE | Deletes a suppression list from Postalytics. |
| [Get Suppression List](actions/get-suppression-list.md) | GET | Retrieves a suppression list from Postalytics. |
| [List Suppression Lists](actions/list-suppression-lists.md) | GET | Retrieves suppression lists from Postalytics. |

### Suppression List Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Suppression List Contact](actions/create-suppression-list-contact.md) | POST | Creates a contact on a Postalytics suppression list. |
| [Delete Suppression List Contact](actions/delete-suppression-list-contact.md) | DELETE | Deletes a contact from a Postalytics suppression list. |
| [Get Suppression List Contact](actions/get-suppression-list-contact.md) | GET | Retrieves a Postalytics suppression-list contact. |
| [List Suppression List Contacts](actions/list-suppression-list-contacts.md) | GET | Retrieves contacts on a Postalytics suppression list. |
| [Update Suppression List Contact](actions/update-suppression-list-contact.md) | PUT | Updates a contact on a Postalytics suppression list. |

