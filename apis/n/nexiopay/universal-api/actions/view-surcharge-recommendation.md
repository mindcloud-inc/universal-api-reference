# Nexiopay: View surcharge recommendation



```
GET https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-surcharge-recommendation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nexiopay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-surcharge-recommendation?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-surcharge-recommendation?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | no | Transaction data object documented by Nexio. |
| `card` | object | no | Card information object documented by Nexio. |
| `tokenex` | object | no | TokenEx payment token object documented by Nexio. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "surchargeAllowed": true,
      "surchargeAmount": 1,
      "totalAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Nexio response message. |
| `surchargeAllowed` | boolean | Whether surcharge is allowed. |
| `surchargeAmount` | number | Recommended surcharge amount. |
| `totalAmount` | number | Total amount including surcharge. |

## Native endpoint

Through the native Nexiopay API, this operation is `POST /pay/v3/surcharge` (base URL `https://api.nexiopaysandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-surcharge-recommendation.md) for the provider-specific parameters and requirements.

