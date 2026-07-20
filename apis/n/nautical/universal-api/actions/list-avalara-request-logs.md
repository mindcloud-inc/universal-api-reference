# Nautical: List Avalara Request Logs

Retrieves a list of Avalara request logs from Nautical.

```
GET https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-avalara-request-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nautical `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-avalara-request-logs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-avalara-request-logs?${params}`, {
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
      "data": {
        "avalaraRequestLogs": {
          "edges": [
            {
              "node": {
                "createdAt": "string",
                "error": "string",
                "id": "string",
                "requestUrl": "https://example.com"
              }
            }
          ],
          "pageInfo": {
            "endCursor": "string",
            "hasNextPage": true
          }
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.avalaraRequestLogs.edges[].node.createdAt` | string |  |
| `data.avalaraRequestLogs.edges[].node.error` | string |  |
| `data.avalaraRequestLogs.edges[].node.id` | string |  |
| `data.avalaraRequestLogs.edges[].node.requestUrl` | string |  |
| `data.avalaraRequestLogs.pageInfo.endCursor` | string |  |
| `data.avalaraRequestLogs.pageInfo.hasNextPage` | boolean |  |

## Native endpoint

Through the native Nautical API, this operation is `POST graphql/` (base URL `https://api.mpconsole.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-avalara-request-logs.md) for the provider-specific parameters and requirements.

