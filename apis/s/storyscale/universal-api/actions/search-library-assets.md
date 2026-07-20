# Storyscale: Search Library Assets



```
GET https://connect.mindcloud.co/v1/universal/storyscale/latest/actions/search-library-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Storyscale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storyscale/latest/actions/search-library-assets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/storyscale/latest/actions/search-library-assets?${params}`, {
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
| `assetTypeId` | number | no | Filter by library asset type. |
| `isFavourite` | boolean | no | Filter to favourite assets. |
| `isSplashImage` | boolean | no | Filter to splash-image assets. |
| `searchVal` | string | no | Filter library assets by a search string. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Filtered library assets payload returned by Storyscale. |
| `status` | object | Top-level API status object. |

## Native endpoint

Through the native Storyscale API, this operation is `GET /v1/library/search` (base URL `https://prodapi.storyscale.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-library-assets.md) for the provider-specific parameters and requirements.

