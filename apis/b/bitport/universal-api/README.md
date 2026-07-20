# <img src="https://images.mindcloud.co/apps/icons/bitport_1776701868356.png" alt="Bitport logo" width="28" height="28"> Bitport: Universal API

Manage cloud files, folders, streams, and transfers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bitport/latest
- **Category:** Content & Files / Storage
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bitport.io
- **Vendor API docs:** https://bitport.io/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitport/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Access Token](actions/get-access-token.md) | POST | Creates a Bitport access token from an access code. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the currently authenticated Bitport user. |

