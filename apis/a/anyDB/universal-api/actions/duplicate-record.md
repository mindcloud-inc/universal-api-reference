# AnyDB: Duplicate Record

Creates a duplicate record in AnyDB.

```
POST https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/duplicate-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AnyDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/duplicate-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recordId": "string",
  "databaseId": "string",
  "teamId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/duplicate-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recordId": "string",
    "databaseId": "string",
    "teamId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recordId` | string | yes | The AnyDB record ID to duplicate. |
| `databaseId` | string | yes | The AnyDB database ID containing the record. |
| `teamId` | string | yes | The AnyDB team ID containing the record. |
| `destinationDatabaseId` | string | no | Optional destination database ID for the duplicate. |
| `attachTo` | string | no | Optional parent ID to attach the duplicate to. |
| `attachmentsMode` | string | no | Optional attachment handling mode: noattachments, link, or duplicate. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AnyDB API returns.

## Native endpoint

Through the native AnyDB API, this operation is `POST /api/integrations/ext/copyrecord` (base URL `https://app.anydb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/duplicate-record.md) for the provider-specific parameters and requirements.

