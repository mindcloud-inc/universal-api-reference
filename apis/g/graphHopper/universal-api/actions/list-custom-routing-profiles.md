# GraphHopper: List Custom Routing Profiles

Retrieves custom routing profiles from GraphHopper.

```
GET https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/list-custom-routing-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GraphHopper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/list-custom-routing-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/list-custom-routing-profiles?${params}`, {
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
      "bounds": {},
      "custom_model": {},
      "id": "string",
      "profile": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounds` | object | Profile bounds. |
| `custom_model` | object | Custom model. |
| `id` | string | Custom profile ID. |
| `profile` | string | Custom profile name. |

## Native endpoint

Through the native GraphHopper API, this operation is `GET /profiles` (base URL `https://graphhopper.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-routing-profiles.md) for the provider-specific parameters and requirements.

