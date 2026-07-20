# Postmark: Get Delivery Stats

Retrieves delivery stats from Postmark.

```
GET https://connect.mindcloud.co/v1/universal/postmark/latest/actions/get-delivery-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmark `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postmark/latest/actions/get-delivery-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postmark/latest/actions/get-delivery-stats?${params}`, {
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
      "InactiveMails": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Bounces[]` | array<object> |  |
| `Bounces[].Count` | number |  |
| `Bounces[].Name` | string |  |
| `Bounces[].Type` | string |  |
| `InactiveMails` | number |  |

## Native endpoint

Through the native Postmark API, this operation is `GET /deliverystats` (base URL `https://api.postmarkapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-delivery-stats.md) for the provider-specific parameters and requirements.

