# <img src="https://images.mindcloud.co/apps/icons/lead2team_1774552326587.png" alt="Lead2Team logo" width="28" height="28"> Lead2Team: Universal API

Read Lead2Team profiles, teams, locations, and widget details

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lead2Team/latest
- **Category:** Support / Contact Center
- **Actions:** 4
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.lead2team.com/
- **Vendor API docs:** https://wiki.lead2team.com/docs-category/add-the-widget-to-your-website/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Widget ID](actions/get-widget-id.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lead2Team/latest/actions/get-widget-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (4)

### Location

| Action | Method | Description |
| --- | --- | --- |
| [List Locations](actions/list-locations.md) | GET |  |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [List Profiles](actions/list-profiles.md) | GET |  |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET |  |

### Widget

| Action | Method | Description |
| --- | --- | --- |
| [Get Widget ID](actions/get-widget-id.md) | GET |  |

