# WorkAdventure: Upload WAM file

Uploads or replaces a WAM file in WorkAdventure map storage.

```
PUT https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/upload-wam-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkAdventure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/upload-wam-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "wamPath": "string",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/upload-wam-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "wamPath": "string",
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `wamPath` | string | yes | Destination WAM file path, including the .wam suffix. |
| `file` | file | yes | URL, base64, or binary content for the WAM file upload. |

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

Through the native WorkAdventure API, this operation is `PUT https://mindcloud-34294.map-storage.workadventu.re/:wamPath` (base URL `https://admin.workadventu.re`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-wam-file.md) for the provider-specific parameters and requirements.

