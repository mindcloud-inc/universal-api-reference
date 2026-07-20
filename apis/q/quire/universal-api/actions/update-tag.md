# Quire: Update Tag

Updates an existing tag in Quire.

```
PUT https://connect.mindcloud.co/v1/universal/quire/latest/actions/update-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/quire/latest/actions/update-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "oid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quire/latest/actions/update-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "oid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `oid` | string | yes | The Quire tag OID. |
| `name` | string | no | The updated display name for the tag. |
| `color` | string | no | Optional updated Quire color code such as 35. |
| `global` | boolean | no | Whether the tag should be available across projects. |
| `project` | string | no | Project OID used only when global is explicitly false. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "name": "Ava Chen",
      "oid": "string",
      "project": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `name` | string |  |
| `oid` | string |  |
| `project` | object |  |

## Native endpoint

Through the native Quire API, this operation is `PUT tag/:oid` (base URL `https://quire.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tag.md) for the provider-specific parameters and requirements.

