# AnyDB: Create Record

Creates a new record in AnyDB.

```
POST https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/create-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AnyDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/create-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "databaseId": "string",
  "teamId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/create-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "databaseId": "string",
    "teamId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `databaseId` | string | yes | The AnyDB database ID. |
| `teamId` | string | yes | The AnyDB team ID. |
| `name` | string | yes | The AnyDB record name. |
| `attachTo` | string | no | Optional AnyDB parent ID to attach the created record to. |
| `template` | string | no | Optional AnyDB template ID for the created record. |
| `templateName` | string | no | Optional AnyDB template name for the created record. |
| `content[]` | array<object> | no | Optional AnyDB content array for the created record. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AnyDB API returns.

## Native endpoint

Through the native AnyDB API, this operation is `POST /api/integrations/ext/createrecord` (base URL `https://app.anydb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-record.md) for the provider-specific parameters and requirements.

