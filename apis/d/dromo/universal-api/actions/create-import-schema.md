# Dromo: Create Import Schema

Creates a new import schema in Dromo.

```
POST https://connect.mindcloud.co/v1/universal/dromo/latest/actions/create-import-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dromo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dromo/latest/actions/create-import-schema" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "fields[]": [
    {}
  ],
  "settings": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dromo/latest/actions/create-import-schema', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "fields[]": [{}],
    "settings": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Request body field name. |
| `fields[]` | array<object> | yes | Request body field fields. |
| `settings` | object | yes | Request body field settings. |
| `hooks` | object | no | Request body field hooks. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dromo API returns.

## Native endpoint

Through the native Dromo API, this operation is `POST /schemas/` (base URL `https://app.dromo.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-import-schema.md) for the provider-specific parameters and requirements.

