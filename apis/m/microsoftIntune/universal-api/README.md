# <img src="https://images.mindcloud.co/apps/icons/microsoft-icon_1776176207568.png" alt="Microsoft Intune logo" width="28" height="28"> Microsoft Intune: Universal API

Manage Microsoft Intune device, app, configuration, and policy resources through Microsoft Graph.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/microsoftIntune/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.microsoft.com/security/business/microsoft-intune
- **Vendor API docs:** https://learn.microsoft.com/en-us/graph/api/resources/intune-graph-overview?view=graph-rest-1.0

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My Profile](actions/get-my-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftIntune/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get My Profile](actions/get-my-profile.md) | GET | Retrieves the signed-in user profile from Microsoft Intune. |

