# Postmark: List Bounces

Retrieves bounces from Postmark.

```
GET https://connect.mindcloud.co/v1/universal/postmark/latest/actions/list-bounces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmark `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postmark/latest/actions/list-bounces?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postmark/latest/actions/list-bounces?${params}`, {
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
      "Bounces": [
        [
          {}
        ]
      ],
      "TotalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Bounces[]` | array<object> |  |
| `Bounces[].BouncedAt` | date |  |
| `Bounces[].CanActivate` | boolean |  |
| `Bounces[].Email` | string |  |
| `Bounces[].ID` | string |  |
| `Bounces[].Inactive` | boolean |  |
| `Bounces[].MessageID` | string |  |
| `Bounces[].Type` | string |  |
| `TotalCount` | number |  |

## Native endpoint

Through the native Postmark API, this operation is `GET /bounces` (base URL `https://api.postmarkapp.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-bounces.md) for the provider-specific parameters and requirements.

