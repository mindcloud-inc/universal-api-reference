# Amberscript: Update Glossary

Updates an existing glossary in Amberscript.

```
PUT https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/update-glossary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amberscript `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/update-glossary" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "glossaryId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amberscript/latest/actions/update-glossary', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "glossaryId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `glossaryId` | string | yes | Glossary to update. |
| `name` | string | yes | Name of the glossary. |
| `names[]` | array<string> | no | Optional array of people, places, or organization names. |
| `items[]` | array<object> | no | Optional array of glossary items with `name` and `description`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Amberscript API returns.

## Native endpoint

Through the native Amberscript API, this operation is `PUT /glossary/:glossaryId` (base URL `https://api.amberscript.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-glossary.md) for the provider-specific parameters and requirements.

