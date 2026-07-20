# Nexiopay: View card token details



```
GET https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-card-token-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nexiopay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-card-token-details?connectionId=$CONNECTION_ID&cardToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cardToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-card-token-details?${params}`, {
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
| `cardToken` | string | yes | Saved card token to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cardType": "string",
      "lastFour": "string",
      "merchantId": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cardType` | string | Card brand/type. |
| `lastFour` | string | Last four card digits. |
| `merchantId` | string | Nexio merchant ID. |
| `token` | string | Saved card token. |

## Native endpoint

Through the native Nexiopay API, this operation is `GET /pay/v3/vault/card/{cardToken}` (base URL `https://api.nexiopaysandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-card-token-details.md) for the provider-specific parameters and requirements.

