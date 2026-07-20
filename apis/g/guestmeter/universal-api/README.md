# <img src="https://images.mindcloud.co/apps/icons/guestmeter_1775068507959.png" alt="Guestmeter logo" width="28" height="28"> Guestmeter: Universal API

Send guest satisfaction surveys and retrieve guest feedback data through Guestmeter's REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/guestmeter/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.guestmeter.com/
- **Vendor API docs:** https://www.guestmeter.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Guests](actions/list-guests.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/guestmeter/latest/actions/list-guests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Guest Satisfaction Response

| Action | Method | Description |
| --- | --- | --- |
| [Get Guest](actions/get-guest.md) | GET | Retrieves guest details from Guestmeter. |
| [List Guests](actions/list-guests.md) | GET | Retrieves guests from Guestmeter. |
| [Send Survey](actions/send-survey.md) | POST | Creates a guest survey request in Guestmeter. |

