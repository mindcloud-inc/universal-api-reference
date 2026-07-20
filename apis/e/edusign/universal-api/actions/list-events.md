# Edusign: List Events

Retrieves events from Edusign.

```
GET https://connect.mindcloud.co/v1/universal/edusign/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/list-events?connectionId=$CONNECTION_ID&page=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "page": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edusign/latest/actions/list-events?${params}`, {
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
| `page` | string | yes | Query param for pagination, starts at page "1" and displays events per page (default: 1) |
| `limit` | string | no | Maximum number of events to return per page (default and max: 1000) |
| `start` | string | no | Filter events starting from this date (format: YYYY-MM-DD, ISO 8601) |
| `end` | string | no | Filter events ending before this date (format: YYYY-MM-DD, ISO 8601) <br><strong>Note:</strong> When both start and end dates are provided, events will be filtered to include only those occurring within this date range. |
| `studentId` | string | no | Show only events assigned to this specific student (use internal Edusign student ID) |
| `professorId` | string | no | Show only events assigned to this specific professor (use internal Edusign professor ID) |
| `apiIds` | string | no | Filter events by external API IDs (JSON array as string, e.g., '["api1","api2"]') |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `light` | string | no | When set to true, returns simplified event data with only id, name, apiId, and apiType fields for faster loading |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "data": [
          {
            "apiId": "string",
            "apiType": "string",
            "classroom": "string",
            "color": "string",
            "description": "string",
            "end": "string",
            "id": "string",
            "name": "Ava Chen",
            "professors": [
              {
                "apiId": "string",
                "professorId": "string"
              }
            ],
            "start": "string",
            "students": [
              {
                "apiId": "string",
                "studentId": "string"
              }
            ]
          }
        ],
        "limit": 1,
        "page": 1,
        "total": 1
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |
| `result.data` | array<object> |  |
| `result.data[].apiId` | string |  |
| `result.data[].apiType` | string |  |
| `result.data[].classroom` | string |  |
| `result.data[].color` | string |  |
| `result.data[].description` | string |  |
| `result.data[].end` | string |  |
| `result.data[].id` | string |  |
| `result.data[].name` | string |  |
| `result.data[].professors` | array<object> |  |
| `result.data[].professors[].apiId` | string |  |
| `result.data[].professors[].professorId` | string |  |
| `result.data[].start` | string |  |
| `result.data[].students` | array<object> |  |
| `result.data[].students[].apiId` | string |  |
| `result.data[].students[].studentId` | string |  |
| `result.limit` | number |  |
| `result.page` | number |  |
| `result.total` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `GET /v1/events` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

