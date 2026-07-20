# Endear: Create Note



```
POST https://connect.mindcloud.co/v1/universal/endear/latest/actions/create-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Endear `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/endear/latest/actions/create-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/endear/latest/actions/create-note', {
  method: 'POST',
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
| `variables.localId` | string | no | Local Id for the Endear GraphQL operation. |
| `variables.creatorId` | string | no | Creator Id for the Endear GraphQL operation. |
| `variables.createdInTeamId` | string | no | Created In Team Id for the Endear GraphQL operation. |
| `variables.customerId` | string | no | Customer Id for the Endear GraphQL operation. |
| `variables.title` | string | no | Title for the Endear GraphQL operation. |
| `variables.description` | string | no | Description for the Endear GraphQL operation. |
| `variables.tags[]` | array<string> | no | Tags for the Endear GraphQL operation. |
| `variables.timeZone` | string | no | Time Zone for the Endear GraphQL operation. |

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

Through the native Endear API, this operation is `POST /graphql` (base URL `https://api.endearhq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-note.md) for the provider-specific parameters and requirements.

