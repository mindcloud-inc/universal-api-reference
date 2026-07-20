# Airtable: Update Multiple Records

Updates multiple records in a specific Airtable table, or upserts them when enabled.

```
PUT https://connect.mindcloud.co/v1/universal/airtable/latest/actions/update-multiple-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airtable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/airtable/latest/actions/update-multiple-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "baseId": "string",
  "tableIdOrName": "Ava Chen",
  "records[]": [
    {}
  ],
  "records[].fields": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airtable/latest/actions/update-multiple-records', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "baseId": "string",
    "tableIdOrName": "Ava Chen",
    "records[]": [{}],
    "records[].fields": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `baseId` | list<string> | yes |  |
| `tableIdOrName` | list<string> | yes |  |
| `records[]` | array<object> | yes | Airtable records array (max 10). Each item must include an id and a fields object. |
| `records[].id` | string | no | Airtable record ID (rec...). Row number is not accepted. Example: `recXXXXXXXXXXXXXX (required for updates; get from List Records)`. |
| `records[].fields` | object | yes | JSON object with field names as keys, e.g. {"name":"Updated"}. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `typecast` | boolean | no | Default: `false`. |
| `returnFieldsByFieldId` | boolean | no | Default: `false`. |
| `performUpsert` | object | no |  |
| `performUpsert.fieldsToMergeOn[]` | array<string> | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Airtable API returns.

## Native endpoint

Through the native Airtable API, this operation is `PATCH /:baseId/:tableIdOrName` (base URL `https://api.airtable.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-multiple-records.md) for the provider-specific parameters and requirements.

