# Dash.app: Get Search Filter View

Retrieves the search filter view from Dash.app.

```
GET https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/get-search-filter-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dash.app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/get-search-filter-view?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/get-search-filter-view?${params}`, {
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
      "permittedActions": [
        {}
      ],
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `permittedActions` | array<object> |  |
| `result` | object |  |

## Native endpoint

Through the native Dash.app API, this operation is `GET /search-filter-view` (base URL `https://api-v2.dash.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-search-filter-view.md) for the provider-specific parameters and requirements.

