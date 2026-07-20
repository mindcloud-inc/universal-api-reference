# WellTraq: List Asset Types

Retrieves asset types from WellTraq.

```
GET https://connect.mindcloud.co/v1/universal/wellTraq/latest/actions/list-asset-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WellTraq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wellTraq/latest/actions/list-asset-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wellTraq/latest/actions/list-asset-types?${params}`, {
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
      "description": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native WellTraq API, this operation is `GET /AssetTypes` (base URL `https://welltraq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-asset-types.md) for the provider-specific parameters and requirements.

