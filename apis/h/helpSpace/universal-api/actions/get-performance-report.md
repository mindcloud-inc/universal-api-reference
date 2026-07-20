# HelpSpace: Get Performance Report

Retrieves a performance report from HelpSpace.

```
GET https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/get-performance-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/get-performance-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpSpace/latest/actions/get-performance-report?${params}`, {
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
      "closed": [
        1
      ],
      "labels": [
        "string"
      ],
      "metrics": [
        {}
      ],
      "opened": [
        1
      ],
      "topAgents": [
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
| `closed` | array<number> |  |
| `labels` | array<string> |  |
| `metrics` | array<object> |  |
| `opened` | array<number> |  |
| `topAgents` | array<object> |  |

## Native endpoint

Through the native HelpSpace API, this operation is `POST /reports/performance` (base URL `https://api.helpspace.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-performance-report.md) for the provider-specific parameters and requirements.

