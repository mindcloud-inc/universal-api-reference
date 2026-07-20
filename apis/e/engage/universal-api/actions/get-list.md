# Engage: Get List

Retrieves a list from Engage by ID.

```
GET https://connect.mindcloud.co/v1/universal/engage/latest/actions/get-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Engage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/engage/latest/actions/get-list?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/engage/latest/actions/get-list?${params}`, {
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
| `id` | string | yes | The Engage list ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "broadcastCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "doubleOptin": true,
      "id": "string",
      "redirectUrl": "https://example.com",
      "subscriberCount": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `broadcastCount` | number |  |
| `createdAt` | date |  |
| `description` | string |  |
| `doubleOptin` | boolean |  |
| `id` | string |  |
| `redirectUrl` | string |  |
| `subscriberCount` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Engage API, this operation is `GET /lists/:id` (base URL `https://api.engage.so/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list.md) for the provider-specific parameters and requirements.

