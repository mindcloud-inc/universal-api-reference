# Pinata: Get Data Usage

Retrieves pinned data usage from Pinata.

```
GET https://connect.mindcloud.co/v1/universal/pinata/latest/actions/get-data-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinata/latest/actions/get-data-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinata/latest/actions/get-data-usage?${params}`, {
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
      "pin_count": 1,
      "pin_size_total": 1,
      "pin_size_with_replications_total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pin_count` | number | Total pinned item count. |
| `pin_size_total` | number | Total pinned bytes. |
| `pin_size_with_replications_total` | number | Pinned bytes including replications. |

## Native endpoint

Through the native Pinata API, this operation is `GET /data/userPinnedDataTotal` (base URL `https://api.pinata.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-usage.md) for the provider-specific parameters and requirements.

