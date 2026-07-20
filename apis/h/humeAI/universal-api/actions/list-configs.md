# Hume AI: List Configs

Retrieves EVI configs from Hume AI.

```
GET https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/list-configs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hume AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/list-configs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/list-configs?${params}`, {
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
      "configsPage": [
        {}
      ],
      "pageNumber": 1,
      "pageSize": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configsPage` | array<object> | Configs returned for the current page. |
| `pageNumber` | number | Current page number. |
| `pageSize` | number | Current page size. |
| `totalPages` | number | Total number of pages. |

## Native endpoint

Through the native Hume AI API, this operation is `GET /v0/evi/configs` (base URL `https://api.hume.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-configs.md) for the provider-specific parameters and requirements.

