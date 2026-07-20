# <img src="https://images.mindcloud.co/apps/icons/favicon-17_1775513768171.png" alt="Poper logo" width="28" height="28"> Poper: Universal API

Build AI-powered popups and widgets to increase onsite engagement, capture leads, and boost conversions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/poper/latest
- **Category:** Marketing
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.poper.ai/
- **Vendor API docs:** https://support.poper.ai/en/collections/10876722-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Verify API Key](actions/verify-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/poper/latest/actions/verify-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Authenticated User

| Action | Method | Description |
| --- | --- | --- |
| [Verify API Key](actions/verify-api-key.md) | GET | Verifies a Poper API key and retrieves the account email. |

### Popup

| Action | Method | Description |
| --- | --- | --- |
| [List Popups](actions/list-popups.md) | GET | Retrieves all popups from your Poper account. |

### Popup Response

| Action | Method | Description |
| --- | --- | --- |
| [List Popup Responses](actions/list-popup-responses.md) | GET | Retrieves responses for a specific Poper popup. |

