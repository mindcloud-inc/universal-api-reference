# fynk: Update Document Dynamic Field

Updates a document dynamic field in fynk.

```
PUT https://connect.mindcloud.co/v1/universal/fynk/latest/actions/update-document-dynamic-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a fynk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fynk/latest/actions/update-document-dynamic-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fynk/latest/actions/update-document-dynamic-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `document` | string | no | Document UUID. Default: `25c718b2-be8b-44e7-858f-3152e7380022`. |
| `dynamicField` | string | no | Dynamic field UUID. Default: `11111111-1111-1111-1111-111111111111`. |
| `value` | string | no | Updated dynamic field value. Default: `test`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native fynk API, this operation is `PUT /documents/:document/dynamic-fields/:dynamicField` (base URL `https://app.fynk.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-document-dynamic-field.md) for the provider-specific parameters and requirements.

