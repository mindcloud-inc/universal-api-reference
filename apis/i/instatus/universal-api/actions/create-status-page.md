# Instatus: Create Status Page



```
POST https://connect.mindcloud.co/v1/universal/instatus/latest/actions/create-status-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instatus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instatus/latest/actions/create-status-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instatus/latest/actions/create-status-page', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | Owner or contact email for the status page. |
| `name` | string | no | Status page name. |
| `subdomain` | string | no | Status page subdomain. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customDomain": "string",
      "id": "string",
      "language": "string",
      "mainStatus": "string",
      "name": "Ava Chen",
      "private": true,
      "status": "string",
      "subdomain": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "websiteUrl": "https://example.com",
      "workspaceId": "string",
      "workspaceSlug": "string"
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
| `language` | string |  |
| `mainStatus` | string |  |
| `name` | string |  |
| `private` | boolean |  |
| `status` | string |  |
| `subdomain` | string |  |
| `updatedAt` | date |  |
| `websiteUrl` | string |  |
| `workspaceId` | string |  |
| `workspaceSlug` | string |  |

## Native endpoint

Through the native Instatus API, this operation is `POST /v1/pages` (base URL `https://api.instatus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-status-page.md) for the provider-specific parameters and requirements.

