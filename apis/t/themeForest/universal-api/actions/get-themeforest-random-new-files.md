# Themeforest: Get ThemeForest Random New Files

Retrieves random new marketplace files from ThemeForest.

```
GET https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-themeforest-random-new-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Themeforest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-themeforest-random-new-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-themeforest-random-new-files?${params}`, {
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
      "items": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> | Random new ThemeForest files. |

## Native endpoint

Through the native Themeforest API, this operation is `GET /v1/market/random-new-files::site.json` (base URL `https://api.envato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-themeforest-random-new-files.md) for the provider-specific parameters and requirements.

