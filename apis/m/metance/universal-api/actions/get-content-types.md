# Metance: Get Content Types

Retrieves content types from the current Metance workspace.

```
GET https://connect.mindcloud.co/v1/universal/metance/latest/actions/get-content-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Metance `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metance/latest/actions/get-content-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metance/latest/actions/get-content-types?${params}`, {
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
      "aiEnabled": true,
      "color": "string",
      "contentsCount": 1,
      "contentTypeName": "Ava Chen",
      "id": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aiEnabled` | boolean | Whether AI is enabled |
| `color` | string | Display color |
| `contentsCount` | number | Contents count |
| `contentTypeName` | string | Content type name |
| `id` | number | Content type ID |
| `status` | number | Content type status |

## Native endpoint

Through the native Metance API, this operation is `GET /contentTypes` (base URL `https://api.metance.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-content-types.md) for the provider-specific parameters and requirements.

