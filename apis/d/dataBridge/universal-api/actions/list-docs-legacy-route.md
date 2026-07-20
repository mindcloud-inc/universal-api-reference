# DataBridge: List Docs (Legacy Route)

Retrieves documents from DataBridge using the legacy route.

```
GET https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/list-docs-legacy-route
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataBridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/list-docs-legacy-route?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/list-docs-legacy-route?${params}`, {
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
      "documents": [
        {}
      ],
      "folderCounts": {},
      "hasMore": true,
      "limit": 1,
      "nextSkip": {},
      "returnedCount": 1,
      "skip": 1,
      "statusCounts": {},
      "totalCount": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documents` | array<object> |  |
| `folderCounts` | object |  |
| `hasMore` | boolean |  |
| `limit` | number |  |
| `nextSkip` | object |  |
| `returnedCount` | number |  |
| `skip` | number |  |
| `statusCounts` | object |  |
| `totalCount` | object |  |

## Native endpoint

Through the native DataBridge API, this operation is `POST /documents/list_docs` (base URL `https://api.morphik.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-docs-legacy-route.md) for the provider-specific parameters and requirements.

