# <img src="https://images.mindcloud.co/apps/icons/church-stamp_1776880568545.png" alt="ChurchStamp logo" width="28" height="28"> ChurchStamp: Universal API

Automated direct-mail follow-up platform for sending ChurchStamp postcard campaigns.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/churchStamp/latest
- **Category:** Marketing
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://churchstamp.com/
- **Vendor API docs:** https://churchstampapi.docs.apiary.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Details](actions/get-user-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/churchStamp/latest/actions/get-user-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Get a Campaign](actions/get-a-campaign.md) | GET | Retrieves campaign details from ChurchStamp by campaign ID. |
| [Get Campaigns](actions/get-campaigns.md) | GET | Retrieves a list of campaigns from ChurchStamp. |

### Campaign Mail

| Action | Method | Description |
| --- | --- | --- |
| [Send Mail](actions/send-mail.md) | POST | Sends campaign mail to a recipient in ChurchStamp. |

### Design

| Action | Method | Description |
| --- | --- | --- |
| [Delete a Design](actions/delete-a-design.md) | DELETE | Deletes an existing design from ChurchStamp by design ID. |
| [Get a Design](actions/get-a-design.md) | GET | Retrieves design details from ChurchStamp by design ID. |
| [Get Designs](actions/get-designs.md) | GET | Retrieves a collection of designs from ChurchStamp. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Details](actions/get-user-details.md) | GET | Retrieves authenticated user details from ChurchStamp. |

