# <img src="https://images.mindcloud.co/apps/icons/favicon-lametric-com-48x48_1776439113102.png" alt="LaMetric logo" width="28" height="28"> LaMetric: Universal API

Manage LaMetric devices, profiles, icons, and local device controls

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/laMetric/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://lametric.com
- **Vendor API docs:** https://lametric-documentation.readthedocs.io/en/latest/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Devices](actions/list-devices.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/laMetric/latest/actions/list-devices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [List Devices](actions/list-devices.md) | GET | Retrieves devices from LaMetric. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User Profile](actions/get-user-profile.md) | GET | Retrieves the current user profile from LaMetric. |

