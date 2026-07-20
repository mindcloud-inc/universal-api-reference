# Mocean API: Request Async Number Lookup



```
GET https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/request-async-number-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mocean API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/request-async-number-lookup?connectionId=$CONNECTION_ID&phoneNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phoneNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/request-async-number-lookup?${params}`, {
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
| `callbackUrl` | string | no | Webhook URL for the asynchronous lookup result. |
| `phoneNumber` | string | yes | The phone number to look up, including country code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentCarrier": {},
      "errMsg": "string",
      "msgid": "string",
      "originalCarrier": {},
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
| `errMsg` | string |  |
| `msgid` | string |  |
| `originalCarrier` | object |  |
| `ported` | string |  |
| `status` | number |  |
| `to` | string |  |

## Native endpoint

Through the native Mocean API API, this operation is `POST /rest/2/nl?mocean-resp-format=json` (base URL `https://rest.moceanapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-async-number-lookup.md) for the provider-specific parameters and requirements.

