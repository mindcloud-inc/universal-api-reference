# <img src="https://images.mindcloud.co/apps/icons/proofly_1775145566688.png" alt="Proofly logo" width="28" height="28"> Proofly: Universal API

Monitor social proof campaigns, notifications, and conversion activity

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/proofly/latest
- **Category:** Marketing
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://proofly.io
- **Vendor API docs:** https://proofly.io/developers

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User](actions/get-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proofly/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Activity](actions/list-activity.md) | GET | Retrieves activity events from your Proofly account. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from your Proofly account. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from your Proofly account. |
| [Toggle Campaign](actions/toggle-campaign.md) | PUT | Toggles a campaign between active and inactive in Proofly. |

### Notification Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Notification Data](actions/get-notification-data.md) | GET | Retrieves notification data from your Proofly account. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves account details from your Proofly account. |

