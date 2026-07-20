# Sakari SMS: List Available Phone Numbers

Finds available phone numbers in Sakari SMS.

```
GET https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/list-available-phone-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sakari SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/list-available-phone-numbers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/list-available-phone-numbers?${params}`, {
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
| `type` | string | no | Phone number type |
| `postalCode` | string | no | Postal code for Number |
| `features` | string | no | Features for phone number |
| `contains` | string | no | What should be in the string |
| `areaCode` | string | no | Area Code for phone number |
| `areaCode` | string | no | Area Code for phone number |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "features": [
        "string"
      ],
      "number": "string",
      "price": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `features` | array<string> |  |
| `number` | string |  |
| `price` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Sakari SMS API, this operation is `GET /v1/accounts/:accountId/availablephonenumbers` (base URL `https://api.sakari.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-phone-numbers.md) for the provider-specific parameters and requirements.

