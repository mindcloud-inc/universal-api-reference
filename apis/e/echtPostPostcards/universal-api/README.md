# <img src="https://images.mindcloud.co/apps/icons/echt-post-postcards_1775248243836.png" alt="EchtPost Postcards logo" width="28" height="28"> EchtPost Postcards: Universal API

Send physical postcards through EchtPost, inspect existing cards, contacts, and templates, and check or top up account credits.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/echtPostPostcards/latest
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://echtpost.de
- **Vendor API docs:** https://hilfe.echtpost.de/article/453/postkartenversand-uber-api-programmierschnittstelle

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credits](actions/get-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/echtPostPostcards/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a saved contact from EchtPost Postcards. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves saved contacts from EchtPost Postcards. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Create Card From Contact](actions/create-card-from-contact.md) | POST | Creates a postcard for one contact in EchtPost Postcards. |
| [Create Card From Contact Data](actions/create-card-from-contact-data.md) | POST | Creates a postcard from contact data in EchtPost Postcards. |
| [Create Card From Contact Group](actions/create-card-from-contact-group.md) | POST | Creates postcards for a contact group in EchtPost Postcards. |
| [Create Card From Contact List](actions/create-card-from-contact-list.md) | POST | Creates postcards for a contact list in EchtPost Postcards. |
| [Delete Card](actions/delete-card.md) | DELETE | Deletes a saved postcard from EchtPost Postcards. |
| [Get Card](actions/get-card.md) | GET | Retrieves a saved postcard from EchtPost Postcards. |
| [List Cards](actions/list-cards.md) | GET | Retrieves saved postcards from EchtPost Postcards. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Get Template](actions/get-template.md) | GET | Retrieves a saved template from EchtPost Postcards. |
| [List Templates](actions/list-templates.md) | GET | Retrieves saved templates from EchtPost Postcards. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Add Credits](actions/add-credits.md) | POST | Adds postcard credits to your EchtPost Postcards account. |
| [Get Credits](actions/get-credits.md) | GET | Retrieves your account balance from EchtPost Postcards. |

