# Greip - Fraud Prevention: Get BIN/IIN Lookup

Retrieves BIN/IIN lookup data from Greip.

```
GET https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-bin-iin-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Greip - Fraud Prevention `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-bin-iin-lookup?connectionId=$CONNECTION_ID&bin=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bin": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-bin-iin-lookup?${params}`, {
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
| `bin` | string | yes | The card BIN or IIN to look up. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bin": "string",
      "blacklisted": true,
      "info": {},
      "isValid": true,
      "reason": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bin` | string |  |
| `blacklisted` | boolean |  |
| `info` | object |  |
| `isValid` | boolean |  |
| `reason` | string |  |

## Native endpoint

Through the native Greip - Fraud Prevention API, this operation is `GET /lookup/bin` (base URL `https://greipapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bin-iin-lookup.md) for the provider-specific parameters and requirements.

