# ESRI: Portal Self

Retrieves the current ArcGIS portal view.

```
GET https://connect.mindcloud.co/v1/universal/eSRI/latest/actions/portal-self
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ESRI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eSRI/latest/actions/portal-self?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eSRI/latest/actions/portal-self?${params}`, {
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
      "access": "string",
      "allSSL": true,
      "id": "string",
      "isPortal": true,
      "name": "Ava Chen",
      "urlKey": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access` | string |  |
| `allSSL` | boolean |  |
| `id` | string |  |
| `isPortal` | boolean |  |
| `name` | string |  |
| `urlKey` | string |  |

## Native endpoint

Through the native ESRI API, this operation is `GET https://www.arcgis.com/sharing/rest/portals/self` (base URL `https://www.arcgis.com/sharing/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/portal-self.md) for the provider-specific parameters and requirements.

