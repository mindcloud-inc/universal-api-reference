# JustCall: Get a Phone Number

Retrieves a phone number from JustCall.

```
GET https://connect.mindcloud.co/v1/universal/justCall/latest/actions/get-a-phone-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JustCall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/justCall/latest/actions/get-a-phone-number?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/justCall/latest/actions/get-a-phone-number?${params}`, {
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
| `id` | number | yes | The JustCall phone number ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availabilitySetting": "string",
      "businessRegistration": "string",
      "capabilities": {},
      "currentStatus": "string",
      "friendlyNumber": "string",
      "id": 1,
      "justcallLineName": "Ava Chen",
      "justcallNumber": "string",
      "numberOwner": {},
      "numberType": "string",
      "sharedWith": {},
      "smsCompliance": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availabilitySetting` | string |  |
| `businessRegistration` | string |  |
| `capabilities` | object |  |
| `currentStatus` | string |  |
| `friendlyNumber` | string |  |
| `id` | number |  |
| `justcallLineName` | string |  |
| `justcallNumber` | string |  |
| `numberOwner` | object |  |
| `numberType` | string |  |
| `sharedWith` | object |  |
| `smsCompliance` | string |  |

## Native endpoint

Through the native JustCall API, this operation is `GET /v2.1/phone-numbers/:id` (base URL `https://api.justcall.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-phone-number.md) for the provider-specific parameters and requirements.

