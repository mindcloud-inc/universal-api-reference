# Bulldog-WP: Get file information

Retrieves file details from Bulldog-WP.

```
GET https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bulldog-WP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-file?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-file?${params}`, {
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
| `fileId` | string | yes | Uploaded file resource ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": "string",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "format": "string",
      "id": "string",
      "lastAccessAt": "2026-05-07T12:00:00.000Z",
      "lastDeliveryAt": "2026-05-07T12:00:00.000Z",
      "origin": "string",
      "permission": 1,
      "status": 1,
      "url": "https://example.com",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact` | string |  |
| `deletedAt` | date |  |
| `expiresAt` | date |  |
| `format` | string |  |
| `id` | string |  |
| `lastAccessAt` | date |  |
| `lastDeliveryAt` | date |  |
| `origin` | string |  |
| `permission` | number |  |
| `status` | number |  |
| `url` | string |  |
| `user` | object |  |

## Native endpoint

Through the native Bulldog-WP API, this operation is `GET /files/{fileId}` (base URL `https://api.bulldog-wp.co.il/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file.md) for the provider-specific parameters and requirements.

