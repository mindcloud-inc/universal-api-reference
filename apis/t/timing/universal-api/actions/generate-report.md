# Timing: Generate Report

Retrieves a time and app usage report from Timing.

```
GET https://connect.mindcloud.co/v1/universal/timing/latest/actions/generate-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timing/latest/actions/generate-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timing/latest/actions/generate-report?${params}`, {
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
| `startDateMin` | string | no |  |
| `startDateMax` | string | no |  |
| `projects[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingStatus": "string",
      "duration": 1,
      "endDate": "2026-05-07T12:00:00.000Z",
      "notes": "string",
      "project": {
        "color": "string",
        "customFields": {},
        "defaultBillingStatus": "string",
        "isArchived": true,
        "notes": "string",
        "parent": "string",
        "productivityScore": 1,
        "self": "string",
        "teamId": "string",
        "title": "string",
        "titleChain": [
          "string"
        ]
      },
      "startDate": "2026-05-07T12:00:00.000Z",
      "title": "string",
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingStatus` | string |  |
| `duration` | number |  |
| `endDate` | date |  |
| `notes` | string |  |
| `project` | object |  |
| `project.color` | string |  |
| `project.customFields` | object |  |
| `project.defaultBillingStatus` | string |  |
| `project.isArchived` | boolean |  |
| `project.notes` | string |  |
| `project.parent` | string |  |
| `project.productivityScore` | number |  |
| `project.self` | string |  |
| `project.teamId` | string |  |
| `project.title` | string |  |
| `project.titleChain` | array<string> |  |
| `startDate` | date |  |
| `title` | string |  |
| `user` | string |  |

## Native endpoint

Through the native Timing API, this operation is `GET /report` (base URL `https://web.timingapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-report.md) for the provider-specific parameters and requirements.

