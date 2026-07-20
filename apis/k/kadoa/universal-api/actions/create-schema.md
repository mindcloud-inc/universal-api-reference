# Kadoa: Create Schema



```
POST https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/create-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kadoa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/create-schema" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fields": "e.g. [{name:\"title\",dataType:\"STRING\",description:\"Title\"}]",
  "name": "Test Schema"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/create-schema', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fields": "e.g. [{name:\"title\",dataType:\"STRING\",description:\"Title\"}]",
    "name": "Test Schema"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entity` | string | no | Entity type Example: `e.g. Product`. |
| `fields` | list<object> | yes | JSON array of field defs Example: `e.g. [{name:"title",dataType:"STRING",description:"Title"}]`. |
| `name` | string | yes | Schema name Default: `Test Schema`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "error": true,
      "message": "string",
      "schemaId": "string",
      "success": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `error` | boolean |  |
| `message` | string |  |
| `schemaId` | string |  |
| `success` | boolean |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Kadoa API, this operation is `POST /v4/schemas/` (base URL `https://api.kadoa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-schema.md) for the provider-specific parameters and requirements.

