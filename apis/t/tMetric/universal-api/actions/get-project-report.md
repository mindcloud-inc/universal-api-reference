# TMetric: Get Project Report



```
GET https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/get-project-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TMetric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/get-project-report?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/get-project-report?${params}`, {
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
| `includeDone` | boolean | no | Include done projects in the report. |
| `projectId` | number<number> | no | Optional list of project identifiers. Accepts multiple values in one string, delimited by `,`. |
| `startDate` | date | no | Report start date. |
| `teamId` | number<number> | no | Optional list of team identifiers. Accepts multiple values in one string, delimited by `,`. |
| `userId` | number<number> | no | Optional list of user identifiers. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billableAmount": 1,
      "billableCurrency": "string",
      "billableSeconds": 1,
      "budget": {
        "spent": 1,
        "total": 1,
        "unit": "string"
      },
      "costAmount": 1,
      "costCurrency": "string",
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
      "totalSeconds": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billableAmount` | number |  |
| `billableCurrency` | string |  |
| `billableSeconds` | number |  |
| `budget.spent` | number |  |
| `budget.total` | number |  |
| `budget.unit` | string |  |
| `costAmount` | number |  |
| `costCurrency` | string |  |
| `project.client.iconUrl` | string |  |
| `project.client.id` | number |  |
| `project.client.name` | string |  |
| `project.iconUrl` | string |  |
| `project.id` | number |  |
| `project.invoiceMethod` | string |  |
| `project.isBillable` | boolean |  |
| `project.name` | string |  |
| `project.status` | string |  |
| `totalSeconds` | number |  |

## Native endpoint

Through the native TMetric API, this operation is `GET /accounts/:accountId/reports/projects` (base URL `https://app.tmetric.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-report.md) for the provider-specific parameters and requirements.

