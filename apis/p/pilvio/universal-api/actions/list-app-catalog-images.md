# Pilvio: List App Catalog Images



```
GET https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-app-catalog-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pilvio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-app-catalog-images?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-app-catalog-images?${params}`, {
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
      "displayName": "Ava Chen",
      "isAppCatalog": true,
      "isDefault": true,
      "osName": "Ava Chen",
      "uiPosition": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string |  |
| `isAppCatalog` | boolean |  |
| `isDefault` | boolean |  |
| `osName` | string |  |
| `uiPosition` | number |  |

## Native endpoint

Through the native Pilvio API, this operation is `GET /config/vm_images/app_catalog` (base URL `https://api.pilvio.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-app-catalog-images.md) for the provider-specific parameters and requirements.

