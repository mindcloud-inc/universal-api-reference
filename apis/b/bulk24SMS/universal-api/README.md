# <img src="https://images.mindcloud.co/apps/icons/logo-2_1775659167380.png" alt="Bulk24SMS logo" width="28" height="28"> Bulk24SMS: Universal API

Use the Bulk24SMS public API for profile lookup, user administration, and balance checks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bulk24SMS/latest
- **Category:** Communication / Team Messaging
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bulk24sms.com/
- **Vendor API docs:** https://api.bulk24sms.com/api_doc/home

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [View Own Profile](actions/view-own-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulk24SMS/latest/actions/view-own-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [View Own Profile](actions/view-own-profile.md) | GET | Retrieves your user profile from Bulk24SMS. |

