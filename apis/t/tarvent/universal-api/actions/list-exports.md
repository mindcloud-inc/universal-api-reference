# Tarvent: List Exports

Retrieves exports from Tarvent.

```
GET https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/list-exports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tarvent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/list-exports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/list-exports?${params}`, {
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
      "createdUtc": "2026-05-07T12:00:00.000Z",
      "downloadUrl": "https://example.com",
      "id": "string",
      "modifiedUtc": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdUtc` | date |  |
| `downloadUrl` | string |  |
| `id` | string |  |
| `modifiedUtc` | date |  |
| `name` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Tarvent API, this operation is `POST /graphql` (base URL `https://api.tarvent.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-exports.md) for the provider-specific parameters and requirements.

