# GrassBlade LRS: Create Statement

Stores a statement in GrassBlade LRS.

```
POST https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/create-statement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrassBlade LRS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/create-statement" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actor.mbox": "string",
  "verb.id": "string",
  "object.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/create-statement', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `actor.mbox` | string | yes | Agent mailbox IRI for the statement actor. |
| `actor.name` | string | no | Human-readable name for the statement actor. |
| `verb.id` | string | yes | Verb IRI for the statement. |
| `object.id` | string | yes | Activity IRI for the statement object. |
| `object.objectType` | string | no | Optional objectType for the Statement object, such as StatementRef when voiding another statement. |
| `context.registration` | string | no | Registration UUID to associate with the statement context. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GrassBlade LRS API returns.

## Native endpoint

Through the native GrassBlade LRS API, this operation is `POST /statements` (base URL `https://test.gblrs.com/xAPI`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-statement.md) for the provider-specific parameters and requirements.

