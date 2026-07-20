# Socket: View Report

Retrieves an uploaded report from Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/view-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/view-report?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/view-report?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "healthy": true,
      "id": "string",
      "issues": [
        {
          "type": "string",
          "value": {
            "category": "string",
            "description": "string",
            "label": "string",
            "locations": "string",
            "props": {},
            "severity": "string",
            "usage": "string"
          }
        }
      ],
      "score": {
        "avgLicense": 1,
        "avgMaintenance": 1,
        "avgQuality": 1,
        "avgSupplyChainRisk": 1,
        "avgVulnerability": 1
      },
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `healthy` | boolean |  |
| `id` | string |  |
| `issues` | array<object> |  |
| `issues[]` | object |  |
| `issues[].type` | string |  |
| `issues[].value` | object |  |
| `issues[].value.category` | string |  |
| `issues[].value.description` | string |  |
| `issues[].value.label` | string |  |
| `issues[].value.locations` | string |  |
| `issues[].value.props` | object |  |
| `issues[].value.severity` | string |  |
| `issues[].value.usage` | string |  |
| `score` | object |  |
| `score.avgLicense` | number |  |
| `score.avgMaintenance` | number |  |
| `score.avgQuality` | number |  |
| `score.avgSupplyChainRisk` | number |  |
| `score.avgVulnerability` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Socket API, this operation is `GET /report/view/:id` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-report.md) for the provider-specific parameters and requirements.

