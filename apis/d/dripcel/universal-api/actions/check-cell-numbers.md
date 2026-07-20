# Dripcel: Check Cell Numbers

Checks whether cell numbers can receive a Dripcel campaign.

```
POST https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/check-cell-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dripcel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/check-cell-numbers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dripcel/latest/actions/check-cell-numbers', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "campaignId": {},
        "creditsUsed": 1,
        "results": [
          {
            "canSend": true,
            "cell": "string"
          }
        ]
      },
      "ok": true,
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.campaignId` | object |  |
| `data.creditsUsed` | number |  |
| `data.results[].canSend` | boolean |  |
| `data.results[].cell` | string |  |
| `ok` | boolean |  |
| `requestId` | string |  |

## Native endpoint

Through the native Dripcel API, this operation is `POST /compliance/send` (base URL `https://api.dripcel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-cell-numbers.md) for the provider-specific parameters and requirements.

