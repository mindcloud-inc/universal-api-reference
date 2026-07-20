# Dromo: Create Headless Import

Creates a new headless import in Dromo.

```
POST https://connect.mindcloud.co/v1/universal/dromo/latest/actions/create-headless-import
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dromo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dromo/latest/actions/create-headless-import" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dromo/latest/actions/create-headless-import', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `schema_id` | string | no | Request body field schema_id. |
| `original_filename` | string | no | Request body field original_filename. |
| `initial_data[]` | array<string> | no | Request body field initial_data. |
| `import_metadata` | object | no | Request body field import_metadata. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dromo API returns.

## Native endpoint

Through the native Dromo API, this operation is `POST /headless/imports/` (base URL `https://app.dromo.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-headless-import.md) for the provider-specific parameters and requirements.

