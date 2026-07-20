# Hume AI: Get Config



```
GET https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/get-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hume AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/get-config?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/humeAI/latest/actions/get-config?${params}`, {
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
| `id` | string | yes | Config ID. |

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

Through the native Hume AI API, this operation is `GET /v0/evi/configs/:id` (base URL `https://api.hume.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-config.md) for the provider-specific parameters and requirements.

