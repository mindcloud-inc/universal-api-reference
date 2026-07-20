# Algolia: Retrieve Log Entries

Retrieves log entries from the Algolia application.

```
GET https://connect.mindcloud.co/v1/universal/algolia/latest/actions/retrieve-log-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/retrieve-log-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/algolia/latest/actions/retrieve-log-entries?${params}`, {
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
| `length` | number | no | Maximum number of log entries to retrieve. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `offset` | number | no | Position of the first log entry to retrieve. |
| `type` | string | no | Log entry type to filter by. |
| `indexName` | string | no | Index name to filter logs by. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "logs": [
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
| `logs` | array<object> |  |

## Native endpoint

Through the native Algolia API, this operation is `GET /1/logs` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-log-entries.md) for the provider-specific parameters and requirements.

