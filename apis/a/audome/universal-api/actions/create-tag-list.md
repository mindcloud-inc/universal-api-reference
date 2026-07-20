# Audome: Create Tag List

Creates a new tag list in Audome.

```
POST https://connect.mindcloud.co/v1/universal/audome/latest/actions/create-tag-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Audome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/audome/latest/actions/create-tag-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Mastering Notes"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/audome/latest/actions/create-tag-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Mastering Notes"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name for the tag list. Example: `Mastering Notes`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Audome API returns.

## Native endpoint

Through the native Audome API, this operation is `POST /tag-lists` (base URL `https://app.audome.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tag-list.md) for the provider-specific parameters and requirements.

