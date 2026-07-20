# iLovePDFv2: Increase Signature Expiration Days



```
PUT https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/increase-signature-expiration-days
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLovePDFv2 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/increase-signature-expiration-days" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tokenRequester": "string",
  "days": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/increase-signature-expiration-days', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tokenRequester": "string",
    "days": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tokenRequester` | string | yes | Signature requester token. |
| `days` | number | yes | Days to add, between 1 and 130. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expires": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expires` | date |  |
| `status` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native iLovePDFv2 API, this operation is `POST /signature/increase-expiration-days/:token_requester` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/increase-signature-expiration-days.md) for the provider-specific parameters and requirements.

