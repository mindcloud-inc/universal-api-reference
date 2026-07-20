# Speak Ai: Create Folder

Creates a folder in Speak Ai.

```
POST https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/create-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Speak Ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Folder name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "folderId": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folderId` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Speak Ai API, this operation is `POST /folder` (base URL `https://api.speakai.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-folder.md) for the provider-specific parameters and requirements.

