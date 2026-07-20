# Themeforest: Get ThemeForest New Files

Retrieves new marketplace files for a ThemeForest category.

```
GET https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-themeforest-new-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Themeforest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-themeforest-new-files?connectionId=$CONNECTION_ID&category=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "category": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/themeForest/latest/actions/get-themeforest-new-files?${params}`, {
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
| `category` | string | yes | ThemeForest category slug. |

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
| `items` | array<object> | New ThemeForest files for the selected category. |

## Native endpoint

Through the native Themeforest API, this operation is `GET /v1/market/new-files::site,:category.json` (base URL `https://api.envato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-themeforest-new-files.md) for the provider-specific parameters and requirements.

