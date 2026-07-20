# Float: Get Projects Report

Retrieves a projects report from Float.

```
GET https://connect.mindcloud.co/v1/universal/float/latest/actions/get-projects-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Float `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/float/latest/actions/get-projects-report?connectionId=$CONNECTION_ID&startDate=string&endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "string",
  "endDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/float/latest/actions/get-projects-report?${params}`, {
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
| `startDate` | string | yes | Start date of the report duration in the format YYYY-MM-DD |
| `endDate` | string | yes | End date of the report duration in the format YYYY-MM-DD |
| `projectId` | number | no | A project ID to filter the response on |

## Response

```json
{
  "success": true,
  "data": [
    {
      "projects": [
        {
          "billable": 1,
          "clientId": {},
          "name": "Ava Chen",
          "nonBillable": 1,
          "projectId": 1,
          "scheduled": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `projects[].billable` | number |  |
| `projects[].clientId` | object |  |
| `projects[].name` | string |  |
| `projects[].nonBillable` | number |  |
| `projects[].projectId` | number |  |
| `projects[].scheduled` | number |  |

## Native endpoint

Through the native Float API, this operation is `GET /reports/projects` (base URL `https://api.float.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-projects-report.md) for the provider-specific parameters and requirements.

