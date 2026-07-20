# Endear: Update Note



```
PUT https://connect.mindcloud.co/v1/universal/endear/latest/actions/update-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Endear `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/endear/latest/actions/update-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/endear/latest/actions/update-note', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.id` | string | yes | Id for the Endear GraphQL operation. |
| `variables.editorId` | string | no | Editor Id for the Endear GraphQL operation. |
| `variables.title` | string | no | Title for the Endear GraphQL operation. |
| `variables.description` | string | no | Description for the Endear GraphQL operation. |
| `variables.tags[]` | array<string> | no | Tags for the Endear GraphQL operation. |
| `variables.customerId` | string | no | Customer Id for the Endear GraphQL operation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Endear API, this operation is `POST /graphql` (base URL `https://api.endearhq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-note.md) for the provider-specific parameters and requirements.

