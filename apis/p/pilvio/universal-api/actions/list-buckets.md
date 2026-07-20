# Pilvio: List Buckets



```
GET https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-buckets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pilvio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-buckets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-buckets?${params}`, {
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
      "billingAccountId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "numObjects": 1,
      "sizeBytes": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingAccountId` | number |  |
| `createdAt` | date |  |
| `name` | string |  |
| `numObjects` | number |  |
| `sizeBytes` | number |  |

## Native endpoint

Through the native Pilvio API, this operation is `GET /storage/bucket/list` (base URL `https://api.pilvio.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-buckets.md) for the provider-specific parameters and requirements.

