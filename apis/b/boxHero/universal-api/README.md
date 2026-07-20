# <img src="https://images.mindcloud.co/apps/icons/boxhero_1774558408723.png" alt="BoxHero logo" width="28" height="28"> BoxHero: Universal API

Track inventory, manage stock, and organize items, partners, and locations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/boxHero/latest
- **Category:** Commerce / Supply Chain
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.boxhero.io
- **Vendor API docs:** https://rest.boxhero-app.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Linked Team](actions/get-linked-team.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/get-linked-team?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Item](actions/create-item.md) | POST | Creates a new item in BoxHero. |
| [Delete Item](actions/delete-item.md) | DELETE | Deletes an existing item from BoxHero. |
| [Get Item](actions/get-item.md) | GET | Retrieves an item from BoxHero. |
| [List Items](actions/list-items.md) | GET | Retrieves items from BoxHero. |
| [Update Item](actions/update-item.md) | PUT | Updates an existing item in BoxHero. |

### Item Attribute

| Action | Method | Description |
| --- | --- | --- |
| [Create Item Attribute](actions/create-item-attribute.md) | POST | Creates a new item attribute in BoxHero. |
| [Get Item Attribute](actions/get-item-attribute.md) | GET | Retrieves an item attribute from BoxHero. |
| [List Item Attributes](actions/list-item-attributes.md) | GET | Retrieves item attributes from BoxHero. |
| [Update Item Attribute](actions/update-item-attribute.md) | PUT | Updates an existing item attribute in BoxHero. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Create Location](actions/create-location.md) | POST | Creates a new location in BoxHero. |
| [Get Location](actions/get-location.md) | GET | Retrieves a location from BoxHero. |
| [List Locations](actions/list-locations.md) | GET | Retrieves locations from BoxHero. |
| [Update Location](actions/update-location.md) | PUT | Updates an existing location in BoxHero. |

### Location Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Create Location Transaction](actions/create-location-transaction.md) | POST |  |
| [Get Location Transaction](actions/get-location-transaction.md) | GET |  |
| [List Location Transactions](actions/list-location-transactions.md) | GET |  |
| [Update Location Transaction](actions/update-location-transaction.md) | PUT |  |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Get Member](actions/get-member.md) | GET | Retrieves a team member from BoxHero. |
| [List Members](actions/list-members.md) | GET | Retrieves team members from BoxHero. |

### Partner

| Action | Method | Description |
| --- | --- | --- |
| [Create Partner](actions/create-partner.md) | POST | Creates a new partner in BoxHero. |
| [Get Partner](actions/get-partner.md) | GET | Retrieves a partner from BoxHero. |
| [List Partners](actions/list-partners.md) | GET | Retrieves partners from BoxHero. |
| [Update Partner](actions/update-partner.md) | PUT | Updates an existing partner in BoxHero. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Get Linked Team](actions/get-linked-team.md) | GET | Retrieves the linked team from BoxHero. |

