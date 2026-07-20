# Heyy: List Attributes

Retrieves attributes from a Heyy workspace.

```
GET https://connect.mindcloud.co/v1/universal/heyy/latest/actions/list-attributes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heyy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyy/latest/actions/list-attributes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heyy/latest/actions/list-attributes?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "externalId": "string",
      "id": "string",
      "name": "Ava Chen",
      "tenantId": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `deletedAt` | date |  |
| `description` | string |  |
| `externalId` | string |  |
| `id` | string |  |
| `name` | string |  |
| `tenantId` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Heyy API, this operation is `GET /attributes` (base URL `https://api.heyy.io/api/v2.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-attributes.md) for the provider-specific parameters and requirements.

