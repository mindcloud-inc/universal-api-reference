# Instatus: Delete Status Page



```
DELETE https://connect.mindcloud.co/v1/universal/instatus/latest/actions/delete-status-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instatus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/instatus/latest/actions/delete-status-page?connectionId=$CONNECTION_ID&pageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instatus/latest/actions/delete-status-page?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageId` | string | yes | Instatus status page ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customDomain": "string",
      "id": "string",
      "name": {},
      "private": true,
      "status": "string",
      "subdomain": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "websiteUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `customDomain` | string |  |
| `id` | string |  |
| `name` | object |  |
| `private` | boolean |  |
| `status` | string |  |
| `subdomain` | string |  |
| `updatedAt` | date |  |
| `websiteUrl` | string |  |

## Native endpoint

Through the native Instatus API, this operation is `DELETE /v2/:page_id` (base URL `https://api.instatus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-status-page.md) for the provider-specific parameters and requirements.

