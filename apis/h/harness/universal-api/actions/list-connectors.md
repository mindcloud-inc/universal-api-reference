# Harness: List Connectors

Retrieves connectors from Harness.

```
GET https://connect.mindcloud.co/v1/universal/harness/latest/actions/list-connectors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harness `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harness/latest/actions/list-connectors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harness/latest/actions/list-connectors?${params}`, {
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
      "empty": true,
      "pageIndex": 1,
      "pageItemCount": 1,
      "pageSize": 1,
      "totalItems": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `empty` | boolean | Whether the page has no connectors. |
| `pageIndex` | number | Zero-based page index. |
| `pageItemCount` | number | Connectors returned in this page. |
| `pageSize` | number | Requested page size. |
| `totalItems` | number | Total number of connectors. |
| `totalPages` | number | Total number of pages. |

## Native endpoint

Through the native Harness API, this operation is `GET /ng/api/connectors` (base URL `https://app.harness.io/gateway`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-connectors.md) for the provider-specific parameters and requirements.

