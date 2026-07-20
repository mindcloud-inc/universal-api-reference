# <img src="https://images.mindcloud.co/apps/icons/ecotrak_1773159935687.png" alt="Ecotrak logo" width="28" height="28"> Ecotrak: Universal API

Manage assets, work orders, invoices, and locations in Ecotrak.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ecotrak/latest
- **Category:** Support / Field Service
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ecotrak.com
- **Vendor API docs:** https://api-docs.ecotrak.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User](actions/get-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ecotrak/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Search Invoices](actions/search-invoices.md) | GET | Finds invoices in Ecotrak by approved or created date. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in Ecotrak. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Ecotrak. |
| [List Users](actions/list-users.md) | GET | Retrieves a list of users from Ecotrak. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Ecotrak. |
| [Update User Assigned Locations](actions/update-user-assigned-locations.md) | PUT | Updates a user's assigned locations in Ecotrak. |

### Work Orders

| Action | Method | Description |
| --- | --- | --- |
| [List Work Orders](actions/list-work-orders.md) | GET | Retrieves work orders updated today from Ecotrak. |
| [Search Work Orders](actions/search-work-orders.md) | GET | Finds work orders in Ecotrak by status or updated date. |

