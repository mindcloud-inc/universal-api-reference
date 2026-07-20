# <img src="https://images.mindcloud.co/apps/icons/a-mcardscom_1774031857421.png" alt="AMcards.com logo" width="28" height="28"> AMcards.com: Universal API

Send greeting cards, manage contacts, and trigger AMcards campaigns

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aMcardscom/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://amcards.com
- **Vendor API docs:** https://staging.amcards.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aMcardscom/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a specific campaign from AMcards.com. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaign records from your AMcards.com account. |

### Card

| Action | Method | Description |
| --- | --- | --- |
| [Get Card](actions/get-card.md) | GET | Retrieves a specific card from AMcards.com. |
| [List Cards](actions/list-cards.md) | GET | Retrieves cards from your AMcards.com account. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Card Template Category](actions/get-card-template-category.md) | GET | Retrieves a specific card template category from AMcards.com. |
| [List Card Template Categories](actions/list-card-template-categories.md) | GET | Retrieves card template categories from AMcards.com. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in AMcards.com. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from AMcards.com. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a specific contact from AMcards.com. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contact records from your AMcards.com account. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in AMcards.com by search query. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in AMcards.com. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new contact group in AMcards.com. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing contact group from AMcards.com. |
| [Get Group](actions/get-group.md) | GET | Retrieves a specific contact group from AMcards.com. |
| [List Groups](actions/list-groups.md) | GET | Retrieves your contact groups from AMcards.com. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing contact group in AMcards.com. |

### Mailing

| Action | Method | Description |
| --- | --- | --- |
| [Get Mailing](actions/get-mailing.md) | GET | Retrieves a specific mailing from AMcards.com. |
| [List Mailings](actions/list-mailings.md) | GET | Retrieves mailings from your AMcards.com account. |

### Public Template

| Action | Method | Description |
| --- | --- | --- |
| [List Public Templates](actions/list-public-templates.md) | GET | Retrieves public card templates from AMcards.com. |

### Quicksend Template

| Action | Method | Description |
| --- | --- | --- |
| [List Quicksend Templates](actions/list-quicksend-templates.md) | GET | Retrieves Quicksend templates from your AMcards.com account. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET | Retrieves template records from your AMcards.com account. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a specific user from AMcards.com. |
| [List Users](actions/list-users.md) | GET | Retrieves authorized user records from AMcards.com. |

