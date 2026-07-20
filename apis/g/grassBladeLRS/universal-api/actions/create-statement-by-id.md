# GrassBlade LRS: Create Statement By ID

Stores a statement by ID in GrassBlade LRS.

```
PUT https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/create-statement-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrassBlade LRS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/create-statement-by-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "statementId": "string",
  "actor.mbox": "string",
  "verb.id": "string",
  "object.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/create-statement-by-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "statementId": "string",
    "actor.mbox": "string",
    "verb.id": "string",
    "object.id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `statementId` | string | yes | Statement ID to store. |
| `actor.mbox` | string | yes | Actor mailbox IRI. |
| `actor.name` | string | no | Actor display name. |
| `verb.id` | string | yes | Verb ID IRI. |
| `object.id` | string | yes | Statement object activity ID. |
| `object.objectType` | string | no | Statement object type when required. |
| `context.registration` | string | no | Registration UUID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GrassBlade LRS API returns.

## Native endpoint

Through the native GrassBlade LRS API, this operation is `PUT /statements` (base URL `https://test.gblrs.com/xAPI`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-statement-by-id.md) for the provider-specific parameters and requirements.

