# WorkAdventure: Get private file

Retrieves a private file from WorkAdventure map storage.

```
GET https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/get-private-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkAdventure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/get-private-file?connectionId=$CONNECTION_ID&filePath=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filePath": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/get-private-file?${params}`, {
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
| `filePath` | string | yes | Private file path to fetch. |

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
| `data` | array<number> | Raw response payload bytes returned by the private file route. |
| `type` | string | Runtime wrapper type for the raw response payload. |

## Native endpoint

Through the native WorkAdventure API, this operation is `GET https://mindcloud-34294.map-storage.workadventu.re/private/files/:filePath` (base URL `https://admin.workadventu.re`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-private-file.md) for the provider-specific parameters and requirements.

