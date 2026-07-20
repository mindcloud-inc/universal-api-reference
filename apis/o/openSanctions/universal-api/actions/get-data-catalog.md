# OpenSanctions: Get Data Catalog



```
GET https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/get-data-catalog
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenSanctions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/get-data-catalog?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openSanctions/latest/actions/get-data-catalog?${params}`, {
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
      "current": [
        "string"
      ],
      "datasets": [
        {}
      ],
      "index_stale": true,
      "outdated": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current` | array<string> | Current dataset scopes. |
| `datasets` | array<object> | Dataset catalog entries. |
| `index_stale` | boolean | Whether the index is stale. |
| `outdated` | array<string> | Outdated dataset scopes. |

## Native endpoint

Through the native OpenSanctions API, this operation is `GET /catalog` (base URL `https://api.opensanctions.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-catalog.md) for the provider-specific parameters and requirements.

