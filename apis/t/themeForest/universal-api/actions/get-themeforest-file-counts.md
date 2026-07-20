# Themeforest: Get ThemeForest File Counts

Retrieves marketplace file counts from ThemeForest.

```
GET https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-themeforest-file-counts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Themeforest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-themeforest-file-counts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-themeforest-file-counts?${params}`, {
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
      "count": 1,
      "site": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of files for the site. |
| `site` | string | Envato site. |

## Native endpoint

Through the native Themeforest API, this operation is `GET /v1/market/number-of-files::site.json` (base URL `https://api.envato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-themeforest-file-counts.md) for the provider-specific parameters and requirements.

