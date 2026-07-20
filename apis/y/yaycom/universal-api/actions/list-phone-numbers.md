# Yay.com: List Phone Numbers

Retrieves phone numbers from Yay.com.

```
GET https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-phone-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yay.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-phone-numbers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yaycom/latest/actions/list-phone-numbers?${params}`, {
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
      "callFlow": "string",
      "canInviteAnonymously": true,
      "countryCode": "string",
      "emergencyAddress": "string",
      "name": "Ava Chen",
      "number": "string",
      "numberAddress": "string",
      "outOfHours": "string",
      "priceCategory": 1,
      "requiredAddressType": 1,
      "trunk": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callFlow` | string |  |
| `canInviteAnonymously` | boolean |  |
| `countryCode` | string |  |
| `emergencyAddress` | string |  |
| `name` | string |  |
| `number` | string |  |
| `numberAddress` | string |  |
| `outOfHours` | string |  |
| `priceCategory` | number |  |
| `requiredAddressType` | number |  |
| `trunk` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Yay.com API, this operation is `GET /voip/number` (base URL `https://api.yay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-phone-numbers.md) for the provider-specific parameters and requirements.

