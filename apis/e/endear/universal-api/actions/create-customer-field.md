# Endear: Create Customer Field



```
POST https://connect.mindcloud.co/v1/universal/endear/latest/actions/create-customer-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Endear `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/endear/latest/actions/create-customer-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.key": "string",
  "variables.label": "string",
  "variables.type": "string",
  "variables.allowMultiple": true,
  "variables.isUserEditable": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/endear/latest/actions/create-customer-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.key": "string",
    "variables.label": "string",
    "variables.type": "string",
    "variables.allowMultiple": true,
    "variables.isUserEditable": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.key` | string | yes | Key for the Endear GraphQL operation. |
| `variables.label` | string | yes | Label for the Endear GraphQL operation. |
| `variables.description` | string | no | Description for the Endear GraphQL operation. |
| `variables.type` | string | yes | Type for the Endear GraphQL operation. |
| `variables.allowMultiple` | boolean | yes | Allow Multiple for the Endear GraphQL operation. |
| `variables.isUserEditable` | boolean | yes | Is User Editable for the Endear GraphQL operation. |
| `variables.order` | string | no | Order for the Endear GraphQL operation. |
| `variables.currency` | string | no | Currency for the Endear GraphQL operation. |
| `variables.customerFieldGroupId` | string | no | Customer Field Group Id for the Endear GraphQL operation. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.options[]` | array<object> | no | Options for the Endear GraphQL operation. |

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

Through the native Endear API, this operation is `POST /graphql` (base URL `https://api.endearhq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-field.md) for the provider-specific parameters and requirements.

