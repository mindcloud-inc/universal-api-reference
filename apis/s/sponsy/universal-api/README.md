# <img src="https://images.mindcloud.co/apps/icons/sponsy_1774625695583.png" alt="Sponsy logo" width="28" height="28"> Sponsy: Universal API

Manage newsletter sponsorships, ad inventory, reporting, and advertiser portals

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sponsy/latest
- **Category:** Marketing / Advertising
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://getsponsy.com
- **Vendor API docs:** https://docs.getsponsy.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Publications](actions/list-publications.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/list-publications?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a customer in Sponsy. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes a customer from Sponsy. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Sponsy. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Sponsy. |
| [Update Customer](actions/update-customer.md) | PUT | Updates a customer in Sponsy. |

### Customer Contact

| Action | Method | Description |
| --- | --- | --- |
| [List Customer Contacts](actions/list-customer-contacts.md) | GET | Retrieves customer contacts from Sponsy. |

### Customer Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Metrics](actions/get-customer-metrics.md) | GET | Retrieves customer metrics from Sponsy. |

### Placement

| Action | Method | Description |
| --- | --- | --- |
| [List Publication Placements](actions/list-publication-placements.md) | GET | Retrieves publication placements from Sponsy. |

### Publication

| Action | Method | Description |
| --- | --- | --- |
| [Get Publication](actions/get-publication.md) | GET | Retrieves a publication from Sponsy. |
| [List Publications](actions/list-publications.md) | GET | Retrieves publications from Sponsy. |

### Publication Placement

| Action | Method | Description |
| --- | --- | --- |
| [Get Publication Placement](actions/get-publication-placement.md) | GET | Retrieves a publication placement from Sponsy. |

### Publication Slot

| Action | Method | Description |
| --- | --- | --- |
| [Create Publication Slot](actions/create-publication-slot.md) | POST | Creates a publication slot in Sponsy. |
| [Get Publication Slot](actions/get-publication-slot.md) | GET | Retrieves a publication slot from Sponsy. |
| [List Customer Slots](actions/list-customer-slots.md) | GET | Retrieves customer slots from Sponsy. |

### Publication Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Publication Status](actions/get-publication-status.md) | GET | Retrieves a publication status from Sponsy. |

### Slot

| Action | Method | Description |
| --- | --- | --- |
| [List Publication Slots](actions/list-publication-slots.md) | GET | Retrieves publication slots from Sponsy. |

### Slot Update Job

| Action | Method | Description |
| --- | --- | --- |
| [Update Publication Slot Price](actions/update-publication-slot-price.md) | PUT | Updates a publication slot price in Sponsy. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [List Publication Statuses](actions/list-publication-statuses.md) | GET | Retrieves publication statuses from Sponsy. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a tag in Sponsy. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes a tag from Sponsy. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from Sponsy. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from Sponsy. |
| [Update Tag](actions/update-tag.md) | PUT | Updates a tag in Sponsy. |

