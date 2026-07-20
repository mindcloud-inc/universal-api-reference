# WorkAdventure: List maps

Retrieves the cached map inventory for a WorkAdventure world.

```
GET https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/list-maps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkAdventure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/list-maps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workAdventure/latest/actions/list-maps?${params}`, {
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
      "maps": {},
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `maps` | object | Map inventory keyed by stored WAM path. |
| `version` | string | Map inventory cache version hash. |

## Native endpoint

Through the native WorkAdventure API, this operation is `GET https://mindcloud-34294.map-storage.workadventu.re/maps` (base URL `https://admin.workadventu.re`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-maps.md) for the provider-specific parameters and requirements.

