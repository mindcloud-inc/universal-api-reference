# WorkAdventure: Ping map storage

Checks whether WorkAdventure map storage is reachable.

```
GET https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/ping-map-storage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkAdventure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/ping-map-storage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/ping-map-storage?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native WorkAdventure API, this operation is `GET https://mindcloud-34294.map-storage.workadventu.re/ping` (base URL `https://admin.workadventu.re`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ping-map-storage.md) for the provider-specific parameters and requirements.

