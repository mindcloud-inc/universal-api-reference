# <img src="https://images.mindcloud.co/apps/icons/charidy_1775681496722.png" alt="Charidy logo" width="28" height="28"> Charidy: Universal API

View Charidy campaigns, donations, and teams in the public API

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/charidy/latest
- **Category:** Marketing
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.charidy.com
- **Vendor API docs:** https://documenter.getpostman.com/view/1118680/S1a4WS4g

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Campaign](actions/get-campaign.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/charidy/latest/actions/get-campaign?connectionId=$CONNECTION_ID&campaignId=96" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from Charidy. |

### Donation

| Action | Method | Description |
| --- | --- | --- |
| [List Campaign Donations](actions/list-campaign-donations.md) | GET | Retrieves donations for a campaign from Charidy. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [List Campaign Teams](actions/list-campaign-teams.md) | GET | Retrieves teams for a campaign from Charidy. |

