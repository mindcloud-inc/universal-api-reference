# Pabbly Hook: Create Folder



```
POST https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/create-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Hook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "New customer webhooks"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "New customer webhooks"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Folder name. Example: `New customer webhooks`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "folder": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folder` | object | Created folder object. |
| `message` | string | Pabbly Hook folder creation confirmation message. |

## Native endpoint

Through the native Pabbly Hook API, this operation is `POST /api/v1/folders` (base URL `https://hook.pabbly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-folder.md) for the provider-specific parameters and requirements.

