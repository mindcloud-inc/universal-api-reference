# WorkAdventure: Upload map archive

Uploads a ZIP archive to WorkAdventure map storage.

```
POST https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/upload-map-archive
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkAdventure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/upload-map-archive" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/upload-map-archive', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | ZIP archive containing map-storage files to upload. |
| `directory` | string | no | Optional target directory inside map storage. |

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
| `data` | array<number> | Byte array containing the raw response payload. |
| `type` | string | Buffer marker returned by the runtime for raw map-storage responses. |

## Native endpoint

Through the native WorkAdventure API, this operation is `POST https://mindcloud-34294.map-storage.workadventu.re/upload` (base URL `https://admin.workadventu.re`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-map-archive.md) for the provider-specific parameters and requirements.

