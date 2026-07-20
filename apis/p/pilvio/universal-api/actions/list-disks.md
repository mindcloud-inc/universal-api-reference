# Pilvio: List Disks



```
GET https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-disks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pilvio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-disks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-disks?${params}`, {
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
      "snapshots": [
        "string"
      ],
      "status": "string",
      "userId": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingAccountId` | number |  |
| `snapshots` | array<string> |  |
| `status` | string |  |
| `userId` | number |  |
| `uuid` | string |  |

## Native endpoint

Through the native Pilvio API, this operation is `GET /storage/disks` (base URL `https://api.pilvio.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-disks.md) for the provider-specific parameters and requirements.

