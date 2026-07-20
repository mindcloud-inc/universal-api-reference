# Histre: Create Or Update Notes

Creates or updates notes in Histre.

```
POST https://connect.mindcloud.co/v1/universal/histre/latest/actions/create-or-update-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Histre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/histre/latest/actions/create-or-update-notes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "notes[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/histre/latest/actions/create-or-update-notes', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "notes[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `append` | string | no | Optional append mode. Use always, dedupe, or true. |
| `attrPriority` | string | no | Optional attribute priority strategy. Use old or new. |
| `notify` | boolean | no | Set false to suppress notifications to users with access to affected collections. |
| `notes[]` | array<object> | yes | Array of one or more Histre note objects to create or update. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Histre API returns.

## Native endpoint

Through the native Histre API, this operation is `POST /api/v1/note/` (base URL `https://histre.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-notes.md) for the provider-specific parameters and requirements.

