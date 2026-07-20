# Dovetail: Create Folder

Creates a new folder in your Dovetail workspace.

```
POST https://connect.mindcloud.co/v1/universal/dovetail/latest/actions/create-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dovetail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dovetail/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dovetail/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Folder title. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dovetail API returns.

## Native endpoint

Through the native Dovetail API, this operation is `POST /v1/folders` (base URL `https://dovetail.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-folder.md) for the provider-specific parameters and requirements.

