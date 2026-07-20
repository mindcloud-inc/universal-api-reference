# Themeforest: Get Catalog Item Version

Retrieves the latest version for an Envato catalog item.

```
GET https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-catalog-item-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Themeforest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-catalog-item-version?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-catalog-item-version?${params}`, {
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
| `id` | number | yes | Envato catalog item ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "wordpress_plugin_latest_version": "string",
      "wordpress_theme_latest_version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `wordpress_plugin_latest_version` | string | Latest WordPress plugin version when available. |
| `wordpress_theme_latest_version` | string | Latest WordPress theme version when available. |

## Native endpoint

Through the native Themeforest API, this operation is `GET /v3/market/catalog/item-version` (base URL `https://api.envato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-catalog-item-version.md) for the provider-specific parameters and requirements.

