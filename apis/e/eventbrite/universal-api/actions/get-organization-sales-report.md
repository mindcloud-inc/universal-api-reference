# Eventbrite: Get Organization Sales Report

Retrieves an organization sales report from Eventbrite.

```
GET https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/get-organization-sales-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/get-organization-sales-report?connectionId=$CONNECTION_ID&endDate=string&eventIds=string&organizationId=string&startDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endDate": "string",
  "eventIds": "string",
  "organizationId": "string",
  "startDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/get-organization-sales-report?${params}`, {
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
| `endDate` | string | yes | End datetime in UTC ISO format. |
| `eventIds` | string | yes | One or more Eventbrite event IDs. |
| `organizationId` | string | yes | Organization identifier. |
| `startDate` | string | yes | Start datetime in UTC ISO format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "date": "string",
          "dateLocalized": "string",
          "totals": {
            "currency": "string",
            "fees": "string",
            "gross": "string",
            "net": "string",
            "quantity": 1
          }
        }
      ],
      "eventIds": [
        "string"
      ],
      "timezone": "string",
      "totals": {
        "currency": "string",
        "fees": "string",
        "gross": "string",
        "net": "string",
        "quantity": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].date` | string |  |
| `data[].dateLocalized` | string |  |
| `data[].totals.currency` | string |  |
| `data[].totals.fees` | string |  |
| `data[].totals.gross` | string |  |
| `data[].totals.net` | string |  |
| `data[].totals.quantity` | number |  |
| `eventIds[]` | string |  |
| `timezone` | string |  |
| `totals.currency` | string |  |
| `totals.fees` | string |  |
| `totals.gross` | string |  |
| `totals.net` | string |  |
| `totals.quantity` | number |  |

## Native endpoint

Through the native Eventbrite API, this operation is `GET /organizations/:organizationId/reports/sales/` (base URL `https://www.eventbriteapi.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-sales-report.md) for the provider-specific parameters and requirements.

