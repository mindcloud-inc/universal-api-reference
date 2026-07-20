# Zoho Sign: Recall Document

Recalls a document in Zoho Sign.

```
PUT https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/recall-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/recall-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "requestId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/recall-document', {
  method: 'PUT',
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
| `requestId` | string | yes | Zoho Sign request identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionTime": 1,
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
| `actionTime` | number |  |
| `code` | number |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Sign API, this operation is `POST /requests/:requestId/recall` (base URL `https://sign.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/recall-document.md) for the provider-specific parameters and requirements.

