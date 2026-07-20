# Airparser: Create Or Update Extraction Schema

Creates or updates an extraction schema in Airparser.

```
PUT https://connect.mindcloud.co/v1/universal/airparser/latest/actions/create-or-update-extraction-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airparser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/airparser/latest/actions/create-or-update-extraction-schema" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inboxId": "string",
  "fields": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airparser/latest/actions/create-or-update-extraction-schema', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inboxId": "string",
    "fields": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inboxId` | string | yes | The Airparser inbox ID. |
| `fields` | list<object> | yes | Array of extraction schema field definitions. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Airparser API returns.

## Native endpoint

Through the native Airparser API, this operation is `POST /inboxes/:inbox_id/schema` (base URL `https://api.airparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-extraction-schema.md) for the provider-specific parameters and requirements.

