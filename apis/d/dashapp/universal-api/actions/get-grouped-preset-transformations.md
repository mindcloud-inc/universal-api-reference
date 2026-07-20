# Dash.app: Get Grouped Preset Transformations

Retrieves grouped preset transformations from Dash.app.

```
GET https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/get-grouped-preset-transformations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dash.app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/get-grouped-preset-transformations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/get-grouped-preset-transformations?${params}`, {
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
      "itemGroupTypes": [
        {}
      ],
      "ungroupedItems": [
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
| `itemGroupTypes` | array<object> |  |
| `ungroupedItems` | array<object> |  |

## Native endpoint

Through the native Dash.app API, this operation is `GET /grouped-preset-transformations` (base URL `https://api-v2.dash.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-grouped-preset-transformations.md) for the provider-specific parameters and requirements.

