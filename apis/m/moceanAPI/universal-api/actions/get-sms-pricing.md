# Mocean API: Get SMS Pricing



```
GET https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/get-sms-pricing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mocean API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/get-sms-pricing?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/get-sms-pricing?${params}`, {
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
| `delimiter` | string | no | Optional CSV delimiter. |
| `mcc` | string | no | Optional mobile country code filter. |
| `mnc` | string | no | Optional mobile network code filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "destinations": [
        {
          "country": "string",
          "currency": "string",
          "mcc": "string",
          "mnc": "string",
          "operator": "string",
          "price": "string"
        }
      ],
      "errMsg": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `destinations` | array<object> |  |
| `destinations[].country` | string |  |
| `destinations[].currency` | string |  |
| `destinations[].mcc` | string |  |
| `destinations[].mnc` | string |  |
| `destinations[].operator` | string |  |
| `destinations[].price` | string |  |
| `errMsg` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Mocean API API, this operation is `GET /rest/2/account/pricing?mocean-resp-format=json&mocean-type=sms` (base URL `https://rest.moceanapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sms-pricing.md) for the provider-specific parameters and requirements.

