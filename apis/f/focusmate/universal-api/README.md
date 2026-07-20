# <img src="https://images.mindcloud.co/apps/icons/favicon-apidocs-focusmate-com-48x48_1777482694667.png" alt="Focusmate logo" width="28" height="28"> Focusmate: Universal API

Access Focusmate profile, partner profile, and session history data through the Focusmate Public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/focusmate/latest
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.focusmate.com/
- **Vendor API docs:** https://apidocs.focusmate.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get My Profile](actions/get-my-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/focusmate/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Partner Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Partner Profile](actions/get-partner-profile.md) | GET | Retrieves a user's public Focusmate profile. |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Get Sessions](actions/get-sessions.md) | GET | Retrieves your Focusmate sessions within a date range. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get My Profile](actions/get-my-profile.md) | GET | Retrieves your personal Focusmate profile data. |

