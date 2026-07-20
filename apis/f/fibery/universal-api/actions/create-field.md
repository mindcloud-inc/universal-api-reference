# Fibery: Create Field

Creates a new field in Fibery.

```
POST https://connect.mindcloud.co/v1/universal/fibery/latest/actions/create-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fibery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fibery/latest/actions/create-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "holderType": "string",
  "name": "Ava Chen",
  "fieldType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fibery/latest/actions/create-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "holderType": "string",
    "name": "Ava Chen",
    "fieldType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `holderType` | string | yes | Type that will receive the new field. |
| `name` | string | yes | New field name including the namespace prefix. |
| `fieldType` | string | yes | Fibery field type, for example `fibery/text`. |
| `meta` | object | no | Optional Fibery field meta object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Fibery API, this operation is `POST /commands` (base URL `https://{{credentials.account}}.fibery.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-field.md) for the provider-specific parameters and requirements.

