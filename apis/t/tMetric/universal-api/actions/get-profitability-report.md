# TMetric: Get Profitability Report



```
GET https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/get-profitability-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TMetric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/get-profitability-report?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/get-profitability-report?${params}`, {
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
| `accountId` | number | yes | Workspace identifier. |
| `clientId` | number<number> | no | Optional list of client identifiers. Accepts multiple values in one string, delimited by `,`. |
| `endDate` | date | no | Report end date. |
| `projectId` | number<number> | no | Optional list of project identifiers. Accepts multiple values in one string, delimited by `,`. |
| `projectManagerId` | number<number> | no | Optional list of project manager identifiers. Accepts multiple values in one string, delimited by `,`. |
| `projectStatus` | string | no | Optional project status filter. |
| `projectType` | string<string> | no | Optional list of project types. Accepts multiple values in one string, delimited by `,`. |
| `startDate` | date | no | Report start date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "project": {
        "client": {
          "iconUrl": "https://example.com",
          "id": 1,
          "name": "Ava Chen"
        },
        "iconUrl": "https://example.com",
        "id": 1,
        "invoiceMethod": "string",
        "isBillable": true,
        "name": "Ava Chen",
        "status": "string"
      },
      "totalBillable": 1,
      "totalCost": 1,
      "user": {
        "iconUrl": "https://example.com",
        "id": 1,
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date |  |
| `project.client.iconUrl` | string |  |
| `project.client.id` | number |  |
| `project.client.name` | string |  |
| `project.iconUrl` | string |  |
| `project.id` | number |  |
| `project.invoiceMethod` | string |  |
| `project.isBillable` | boolean |  |
| `project.name` | string |  |
| `project.status` | string |  |
| `totalBillable` | number |  |
| `totalCost` | number |  |
| `user.iconUrl` | string |  |
| `user.id` | number |  |
| `user.name` | string |  |

## Native endpoint

Through the native TMetric API, this operation is `GET /accounts/:accountId/reports/profitability` (base URL `https://app.tmetric.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-profitability-report.md) for the provider-specific parameters and requirements.

