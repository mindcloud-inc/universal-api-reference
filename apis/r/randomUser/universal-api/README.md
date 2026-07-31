# <img src="https://images.mindcloud.co/apps/icons/random-user_1785420756054.png" alt="Random User logo" width="28" height="28"> Random User: Universal API

Generate synthetic user profiles for application testing

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/randomUser/latest
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://randomuser.me/
- **Vendor API docs:** https://randomuser.me/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Generate Random Users](actions/generate-random-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/randomUser/latest/actions/generate-random-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Generate Random Users](actions/generate-random-users.md) | GET |  |

