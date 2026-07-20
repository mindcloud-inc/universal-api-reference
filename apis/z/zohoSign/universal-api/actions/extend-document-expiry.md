# Zoho Sign: Extend Document Expiry

Extends document expiry in Zoho Sign.

```
PUT https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/extend-document-expiry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/extend-document-expiry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "requestId": "string",
  "expireBy": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/extend-document-expiry', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "requestId": "string",
    "expireBy": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `requestId` | string | yes | Zoho Sign request identifier. |
| `expireBy` | string | yes | New expiry date for the document, for example 30 November 2024. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Sign API, this operation is `PUT /requests/:requestId/extend` (base URL `https://sign.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extend-document-expiry.md) for the provider-specific parameters and requirements.

