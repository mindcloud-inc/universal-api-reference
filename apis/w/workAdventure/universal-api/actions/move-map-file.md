# WorkAdventure: Move map file

Moves a file in WorkAdventure map storage.

```
PUT https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/move-map-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkAdventure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/move-map-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "source": "string",
  "destination": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/move-map-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "source": "string",
    "destination": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `source` | string | yes | Existing map-storage file path to move from. |
| `destination` | string | yes | New map-storage file path to move to. |

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

Through the native WorkAdventure API, this operation is `POST https://mindcloud-34294.map-storage.workadventu.re/move` (base URL `https://admin.workadventu.re`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-map-file.md) for the provider-specific parameters and requirements.

