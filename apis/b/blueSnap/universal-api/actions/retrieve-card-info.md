# BlueSnap: Retrieve Card Info

Retrieves card information from BlueSnap.

```
GET https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/retrieve-card-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlueSnap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/retrieve-card-info?connectionId=$CONNECTION_ID&cardNumber=411111" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cardNumber": "411111"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/retrieve-card-info?${params}`, {
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
| `cardNumber` | string | yes | Card BIN or card number to resolve metadata. Default: `411111`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "binCategory": "string",
      "cardCategory": "string",
      "cardRegulated": "string",
      "cardType": "string",
      "issuingBank": "string",
      "issuingCountryCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `binCategory` | string | BIN category. |
| `cardCategory` | string | Card category. |
| `cardRegulated` | string | Regulation indicator. |
| `cardType` | string | Card brand. |
| `issuingBank` | string | Issuing bank name. |
| `issuingCountryCode` | string | Issuing country ISO code. |

## Native endpoint

Through the native BlueSnap API, this operation is `POST /tools/credit-card-info-resolver` (base URL `https://sandbox.bluesnap.com/services/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-card-info.md) for the provider-specific parameters and requirements.

