# Airparser: Clone Extraction Schema

Clones an extraction schema between Airparser inboxes.

```
POST https://connect.mindcloud.co/v1/universal/airparser/latest/actions/clone-extraction-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airparser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/airparser/latest/actions/clone-extraction-schema" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inboxId": "string",
  "destinationInboxId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airparser/latest/actions/clone-extraction-schema', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inboxId": "string",
    "destinationInboxId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inboxId` | string | yes | The source Airparser inbox ID. |
| `destinationInboxId` | string | yes | The destination inbox ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Airparser API returns.

## Native endpoint

Through the native Airparser API, this operation is `POST /inboxes/:inbox_id/schema-clone` (base URL `https://api.airparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clone-extraction-schema.md) for the provider-specific parameters and requirements.

