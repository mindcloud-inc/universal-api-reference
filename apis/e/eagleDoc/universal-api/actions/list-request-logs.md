# Eagle Doc: List Request Logs

Retrieves API request logs from Eagle Doc.

```
GET https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/list-request-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eagle Doc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/list-request-logs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/list-request-logs?${params}`, {
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
      "fileHash": "string",
      "otherInfo": {
        "docType": "string",
        "url": "https://example.com"
      },
      "pages": 1,
      "time": "2026-05-07T12:00:00.000Z",
      "timeRequested": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileHash` | string |  |
| `otherInfo.docType` | string |  |
| `otherInfo.url` | string |  |
| `pages` | number |  |
| `time` | date |  |
| `timeRequested` | date |  |

## Native endpoint

Through the native Eagle Doc API, this operation is `GET /api/usage/v1/logs` (base URL `https://de.eagle-doc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-request-logs.md) for the provider-specific parameters and requirements.

