# <img src="https://images.mindcloud.co/apps/icons/hey-poplar_1774553066452.png" alt="HeyPoplar logo" width="28" height="28"> HeyPoplar: Universal API

Send direct mail, manage audiences, and track customer orders

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/heyPoplar/latest
- **Category:** Marketing
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://heypoplar.com
- **Vendor API docs:** https://docs.heypoplar.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Organization](actions/get-current-organization.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/get-current-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Audience

| Action | Method | Description |
| --- | --- | --- |
| [List Audiences](actions/list-audiences.md) | GET | Retrieves audiences from HeyPoplar. |

### Audience Member

| Action | Method | Description |
| --- | --- | --- |
| [Create Audience Member](actions/create-audience-member.md) | POST | Creates an audience member in HeyPoplar. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from HeyPoplar. |
| [List Active Campaigns](actions/list-active-campaigns.md) | GET | Retrieves active campaigns from HeyPoplar. |

### Campaign Creative

| Action | Method | Description |
| --- | --- | --- |
| [List Campaign Creatives](actions/list-campaign-creatives.md) | GET | Retrieves creatives for a HeyPoplar campaign. |

### Data Subject Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Data Subject Request](actions/create-data-subject-request.md) | POST | Creates a data subject request in HeyPoplar. |
| [Get Data Subject Request Status](actions/get-data-subject-request-status.md) | GET | Retrieves a data subject request status from HeyPoplar. |

### Do Not Mail Entry

| Action | Method | Description |
| --- | --- | --- |
| [Add Do Not Mail Entry](actions/add-do-not-mail-entry.md) | POST | Creates a do-not-mail entry in HeyPoplar. |

### Mailing

| Action | Method | Description |
| --- | --- | --- |
| [Create Mailer](actions/create-mailer.md) | POST | Creates a new mailer in HeyPoplar. |
| [Get Mailing](actions/get-mailing.md) | GET | Retrieves a mailing from HeyPoplar. |
| [List Campaign Mailings](actions/list-campaign-mailings.md) | GET | Retrieves mailings for a HeyPoplar campaign. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Create Order](actions/create-order.md) | POST | Creates a new order in HeyPoplar. |
| [Delete Order](actions/delete-order.md) | DELETE | Deletes an order from HeyPoplar. |
| [Update Order](actions/update-order.md) | PUT | Updates an existing order in HeyPoplar. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Organization](actions/get-current-organization.md) | GET | Retrieves the current organization from HeyPoplar. |

