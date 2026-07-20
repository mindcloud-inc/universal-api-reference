# WorkAdventure: Delete map file

Deletes a file from WorkAdventure map storage.

```
DELETE https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/delete-map-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkAdventure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/delete-map-file?connectionId=$CONNECTION_ID&filePath=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filePath": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/delete-map-file?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filePath` | string | yes | Map-storage file path to delete. |

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

Through the native WorkAdventure API, this operation is `DELETE https://mindcloud-34294.map-storage.workadventu.re/:filePath` (base URL `https://admin.workadventu.re`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-map-file.md) for the provider-specific parameters and requirements.

