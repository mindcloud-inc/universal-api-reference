# WorkAdventure: Upload file

Uploads or replaces a file in WorkAdventure map storage.

```
PUT https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/upload-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkAdventure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/upload-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "filePath": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/upload-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "filePath": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | File content to upload. |
| `filePath` | string | yes | Stored file path to upload or replace. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | Raw response payload bytes returned by map storage. |
| `type` | string | Runtime wrapper type for the raw response payload. |

## Native endpoint

Through the native WorkAdventure API, this operation is `PUT https://mindcloud-34294.map-storage.workadventu.re/:filePath` (base URL `https://admin.workadventu.re`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-file.md) for the provider-specific parameters and requirements.

