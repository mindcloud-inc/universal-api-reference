# RightSignature: Update Document PIN

Updates the PIN for an existing RightSignature document.

```
PUT https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/update-document-pin
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RightSignature `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/update-document-pin" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pin": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/update-document-pin', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pin": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pin` | string | yes | Document pin. Must be between 10000 and 99999 |
| `id` | string | yes | Id value |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RightSignature API returns.

## Native endpoint

Through the native RightSignature API, this operation is `PUT /documents/:id/update_pin` (base URL `https://api.rightsignature.com/public/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-document-pin.md) for the provider-specific parameters and requirements.

