# HotspotSystem: List Location Options

Retrieves the resource owner's locations as options from HotspotSystem.

```
GET https://connect.mindcloud.co/v1/universal/hotspotSystem/latest/actions/list-location-options
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HotspotSystem `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hotspotSystem/latest/actions/list-location-options?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hotspotSystem/latest/actions/list-location-options?${params}`, {
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
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Location option ID. |
| `name` | string | Location option label. |

## Native endpoint

Through the native HotspotSystem API, this operation is `GET /locations/options` (base URL `https://api.hotspotsystem.com/v2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-location-options.md) for the provider-specific parameters and requirements.

