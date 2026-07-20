# ShipWise: List Channels

Retrieves channels from ShipWise.

```
GET https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/list-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShipWise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/list-channels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/list-channels?${params}`, {
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
      "id": "string",
      "marketplace": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Channel identifier. |
| `marketplace` | string | Marketplace or integration name when returned. |
| `name` | string | Channel name. |

## Native endpoint

Through the native ShipWise API, this operation is `GET /api/v1/Channel` (base URL `https://api.shipwise.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-channels.md) for the provider-specific parameters and requirements.

