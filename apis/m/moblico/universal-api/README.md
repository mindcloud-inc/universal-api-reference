# <img src="https://images.mindcloud.co/apps/icons/moblico-logo-dark_1783352603959.png" alt="Moblico logo" width="28" height="28"> Moblico: Universal API

Manage Moblico users, settings, and mobile engagement data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/moblico/latest
- **Category:** Marketing
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.moblicosolutions.com
- **Vendor API docs:** https://client.moblico.net/developer/trialtpl/signup.jsp

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check User Exists](actions/check-user-exists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moblico/latest/actions/check-user-exists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Check User Exists](actions/check-user-exists.md) | GET |  |
| [Create User ID](actions/create-user-id.md) | GET |  |
| [Get User](actions/get-user.md) | GET |  |

