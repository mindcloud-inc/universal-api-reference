# Zoho Sign: Create Document Type

Creates a document type in Zoho Sign.

```
POST https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/create-document-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/create-document-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {},
  "data.requestTypes": {},
  "data.requestTypes.requestTypeName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/create-document-type', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {},
    "data.requestTypes": {},
    "data.requestTypes.requestTypeName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | yes | Zoho Sign document type payload wrapper. |
| `data.requestTypes` | object | yes | Document type details. |
| `data.requestTypes.requestTypeName` | string | yes | Name of the document type to create. |
| `data.requestTypes.requestTypeDescription` | string | no | Description of the document type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "message": "string",
      "requestTypes": [
        {
          "requestTypeDescription": "string",
          "requestTypeId": "string",
          "requestTypeName": "Ava Chen"
        }
      ],
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
| `requestTypes` | array<object> |  |
| `requestTypes[].requestTypeDescription` | string |  |
| `requestTypes[].requestTypeId` | string |  |
| `requestTypes[].requestTypeName` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Sign API, this operation is `POST /requesttypes` (base URL `https://sign.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document-type.md) for the provider-specific parameters and requirements.

