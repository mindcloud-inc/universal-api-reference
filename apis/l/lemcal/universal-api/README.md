# <img src="https://images.mindcloud.co/apps/icons/lemcal-icon-filled-256_1774549115549.png" alt="Lemcal logo" width="28" height="28"> Lemcal: Universal API

Lemcal is a scheduling platform for managing meeting types, booked meetings, and webhooks through the Lemcal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lemcal/latest
- **Category:** Productivity / Scheduling
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.lemcal.com
- **Vendor API docs:** https://developer.lemcal.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate Authentication](actions/validate-authentication.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lemcal/latest/actions/validate-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Hooks

| Action | Method | Description |
| --- | --- | --- |
| [Create Hook](actions/create-hook.md) | POST | Creates a new hook in Lemcal. |
| [Delete Hook](actions/delete-hook.md) | DELETE | Deletes an existing hook from Lemcal. |

### Meeting Types

| Action | Method | Description |
| --- | --- | --- |
| [Get Meeting Type](actions/get-meeting-type.md) | GET | Retrieves a meeting type from Lemcal. |
| [List Meeting Types](actions/list-meeting-types.md) | GET | Retrieves your meeting types from Lemcal. |
| [Validate Authentication](actions/validate-authentication.md) | GET | Retrieves the authenticated user from Lemcal. |

### Meetings

| Action | Method | Description |
| --- | --- | --- |
| [List Booked Meetings](actions/list-booked-meetings.md) | GET | Retrieves your booked meetings from Lemcal. |

