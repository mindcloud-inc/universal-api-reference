# Mocean API: Resend Verify Code SMS With Lookup



```
POST https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/resend-verify-code-sms-with-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mocean API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/resend-verify-code-sms-with-lookup" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "requestId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/resend-verify-code-sms-with-lookup', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "requestId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `requestId` | string | yes | Verify request ID returned by Mocean. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "countryCode": "string",
      "error": "string",
      "networkCode": "string",
      "requestId": "string",
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
| `countryCode` | string |  |
| `error` | string |  |
| `networkCode` | string |  |
| `requestId` | string |  |
| `status` | number |  |
| `to` | string |  |

## Native endpoint

Through the native Mocean API API, this operation is `POST /rest/2/verify/resend/sms?mocean-resp-format=json&mocean-request-nl=1` (base URL `https://rest.moceanapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resend-verify-code-sms-with-lookup.md) for the provider-specific parameters and requirements.

