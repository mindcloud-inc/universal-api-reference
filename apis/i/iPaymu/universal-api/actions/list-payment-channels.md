# iPaymu: List Payment Channels

List available iPaymu payment channels.

```
GET https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/list-payment-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iPaymu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/list-payment-channels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/list-payment-channels?${params}`, {
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
      "channels": [
        {
          "code": "string",
          "description": "string",
          "featureStatus": "string",
          "healthStatus": "string",
          "logo": "string",
          "name": "Ava Chen",
          "paymentInstructionsDoc": "string",
          "transactionFee": {
            "actualFee": 1,
            "actualFeeType": "string",
            "additionalFee": 1
          }
        }
      ],
      "code": "string",
      "description": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channels[].code` | string |  |
| `channels[].description` | string |  |
| `channels[].featureStatus` | string |  |
| `channels[].healthStatus` | string |  |
| `channels[].logo` | string |  |
| `channels[].name` | string |  |
| `channels[].paymentInstructionsDoc` | string |  |
| `channels[].transactionFee.actualFee` | number |  |
| `channels[].transactionFee.actualFeeType` | string |  |
| `channels[].transactionFee.additionalFee` | number |  |
| `code` | string |  |
| `description` | string |  |
| `name` | string |  |

## Native endpoint

Through the native iPaymu API, this operation is `GET /payment-channels` (base URL `https://my.ipaymu.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payment-channels.md) for the provider-specific parameters and requirements.

