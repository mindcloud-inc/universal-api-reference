# Mocean API: Request Number Lookup



```
GET https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/request-number-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mocean API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/request-number-lookup?connectionId=$CONNECTION_ID&phoneNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phoneNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/request-number-lookup?${params}`, {
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
| `phoneNumber` | string | yes | The phone number to look up, including country code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentCarrier": {
        "country": "string",
        "mcc": "string",
        "mnc": "string",
        "name": "Ava Chen",
        "networkCode": 1
      },
      "errMsg": "string",
      "msgid": "string",
      "originalCarrier": {
        "country": "string",
        "mcc": "string",
        "mnc": "string",
        "name": "Ava Chen",
        "networkCode": 1
      },
      "ported": "string",
      "status": 1,
      "to": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentCarrier` | object |  |
| `currentCarrier.country` | string |  |
| `currentCarrier.mcc` | string |  |
| `currentCarrier.mnc` | string |  |
| `currentCarrier.name` | string |  |
| `currentCarrier.networkCode` | number |  |
| `errMsg` | string |  |
| `msgid` | string |  |
| `originalCarrier` | object |  |
| `originalCarrier.country` | string |  |
| `originalCarrier.mcc` | string |  |
| `originalCarrier.mnc` | string |  |
| `originalCarrier.name` | string |  |
| `originalCarrier.networkCode` | number |  |
| `ported` | string |  |
| `status` | number |  |
| `to` | string |  |

## Native endpoint

Through the native Mocean API API, this operation is `POST /rest/2/nl?mocean-resp-format=json` (base URL `https://rest.moceanapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-number-lookup.md) for the provider-specific parameters and requirements.

