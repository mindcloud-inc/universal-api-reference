# Column: Link Associated Person



```
POST https://connect.mindcloud.co/v1/universal/column/latest/actions/link-associated-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Column `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/column/latest/actions/link-associated-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entityId": "string",
  "personEntityId": "string",
  "roles[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/column/latest/actions/link-associated-person', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entityId": "string",
    "personEntityId": "string",
    "roles[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entityId` | string | yes | ID of the business entity. |
| `personEntityId` | string | yes | ID of the person entity to associate. |
| `roles[]` | array<string> | yes | Roles of the person in the business. |
| `titleInBusiness` | string | no | Job title or role of the person in the business. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Column API returns.

## Native endpoint

Through the native Column API, this operation is `POST /entities/:entity_id/associated-persons` (base URL `https://api.column.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/link-associated-person.md) for the provider-specific parameters and requirements.

