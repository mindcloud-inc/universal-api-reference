# Synchroteam: List Shared Blocks

Retrieves a list of shared blocks from Synchroteam.

```
GET https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/list-shared-blocks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Synchroteam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/list-shared-blocks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/synchroteam/latest/actions/list-shared-blocks?${params}`, {
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
      "flPublished": 1,
      "flShared": 1,
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `flPublished` | number |  |
| `flShared` | number |  |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Synchroteam API, this operation is `GET /Api/v2/SharedBlocks/List` (base URL `https://ws.synchroteam.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shared-blocks.md) for the provider-specific parameters and requirements.

