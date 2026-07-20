# <img src="https://images.mindcloud.co/apps/icons/id-kwm3wwj-n-1774465550426_1774465555124.jpeg" alt="Leadfox logo" width="28" height="28"> Leadfox: Universal API

Capture leads, automate marketing, and manage customer campaigns

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/leadfox/latest
- **Category:** Marketing
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.leadfox.co/
- **Vendor API docs:** https://cdn.leadfox.co/upload/7/api_leadfox_12_12-2017.pdf

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Lists](actions/list-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadfox/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Delete Contact](actions/delete-contact.md) | DELETE |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Contact History

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact History](actions/get-contact-history.md) | GET |  |

### List

| Action | Method | Description |
| --- | --- | --- |
| [List Lists](actions/list-lists.md) | GET |  |

