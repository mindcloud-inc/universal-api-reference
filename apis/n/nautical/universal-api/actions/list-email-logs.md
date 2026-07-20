# Nautical: List Email Logs

Retrieves a list of email logs from Nautical.

```
GET https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-email-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nautical `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-email-logs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-email-logs?${params}`, {
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
        "emailLogs": {
          "edges": [
            {
              "node": {
                "date": "ava@example.com",
                "fromEmail": "ava@example.com",
                "id": "ava@example.com",
                "messageType": "ava@example.com"
              }
            }
          ],
          "pageInfo": {
            "endCursor": "ava@example.com",
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
| `data.emailLogs.edges[].node.date` | string |  |
| `data.emailLogs.edges[].node.fromEmail` | string |  |
| `data.emailLogs.edges[].node.id` | string |  |
| `data.emailLogs.edges[].node.messageType` | string |  |
| `data.emailLogs.pageInfo.endCursor` | string |  |
| `data.emailLogs.pageInfo.hasNextPage` | boolean |  |

## Native endpoint

Through the native Nautical API, this operation is `POST graphql/` (base URL `https://api.mpconsole.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-email-logs.md) for the provider-specific parameters and requirements.

