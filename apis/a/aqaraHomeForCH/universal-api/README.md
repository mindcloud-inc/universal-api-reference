# <img src="https://images.mindcloud.co/apps/icons/aqara_1777387017999.png" alt="Aqara Home for CH logo" width="28" height="28"> Aqara Home for CH: Universal API

Connect Aqara Home for China Mainland through Aqara's signed Open Platform APIs for authorization, device, scene, linkage, IR, firmware, and position management.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aqaraHomeForCH/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.aqara.com/
- **Vendor API docs:** https://opendoc.aqara.com/en/docs/developmanual/processOverview.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Positions](actions/list-positions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aqaraHomeForCH/latest/actions/list-positions?connectionId=$CONNECTION_ID&data=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Get Access Token](actions/get-access-token.md) | POST | Creates Aqara access and refresh tokens from an authorization code. |
| [Get Authorization Code](actions/get-authorization-code.md) | POST | Retrieves an Aqara authorization code for account access. |
| [Refresh Access Token](actions/refresh-access-token.md) | PUT | Refreshes Aqara access and refresh tokens with a refresh token. |

### Positions

| Action | Method | Description |
| --- | --- | --- |
| [Create Position](actions/create-position.md) | POST | Creates a new position in Aqara Home for CH. |
| [Delete Position](actions/delete-position.md) | DELETE | Deletes an existing position from Aqara Home for CH. |
| [Get Position Details](actions/get-position-details.md) | GET | Retrieves Aqara Home for CH position details by ID. |
| [List Positions](actions/list-positions.md) | GET | Retrieves subordinate positions from Aqara Home for CH. |
| [Update Position](actions/update-position.md) | PUT | Updates an existing position in Aqara Home for CH. |

