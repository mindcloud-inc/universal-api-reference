# Zoho PageSense: Individual Stats Report

Retrieves an individual stats report from Zoho PageSense.

```
GET https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/individual-stats-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho PageSense `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/individual-stats-report?connectionId=$CONNECTION_ID&limit=25&offset=0&portalName=Ava%20Chen&fullTrackingReports.startDate=2026-05-07T12%3A00%3A00.000Z&fullTrackingReports.endDate=2026-05-07T12%3A00%3A00.000Z&fullTrackingReports.primaryDimension=string&fullTrackingReports.metrics=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "portalName": "Ava Chen",
  "fullTrackingReports.startDate": "2026-05-07T12:00:00.000Z",
  "fullTrackingReports.endDate": "2026-05-07T12:00:00.000Z",
  "fullTrackingReports.primaryDimension": "string",
  "fullTrackingReports.metrics": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/individual-stats-report?${params}`, {
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
| `portalName` | string | yes | Portal identifier in the path. |
| `fullTrackingReports.startDate` | date | yes | Report start date in YYYY-MM-DD format. |
| `fullTrackingReports.endDate` | date | yes | Report end date in YYYY-MM-DD format. |
| `fullTrackingReports.primaryDimension` | string | yes | Dimension to group metrics by. |
| `fullTrackingReports.metrics` | list<string> | yes | Requested metric keys. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "fullTrackingReports": [
        {
          "averageTimeOnPage": 1,
          "bounceRate": 1,
          "entrances": 1,
          "exitRate": 1,
          "pageViews": 1,
          "primaryDimension": "string",
          "uniquePageViews": 1
        }
      ],
      "statusCode": "string",
      "statusString": "string",
      "timeTakenToProcessTheRequest": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `fullTrackingReports[].averageTimeOnPage` | number |  |
| `fullTrackingReports[].bounceRate` | number |  |
| `fullTrackingReports[].entrances` | number |  |
| `fullTrackingReports[].exitRate` | number |  |
| `fullTrackingReports[].pageViews` | number |  |
| `fullTrackingReports[].primaryDimension` | string |  |
| `fullTrackingReports[].uniquePageViews` | number |  |
| `statusCode` | string |  |
| `statusString` | string |  |
| `timeTakenToProcessTheRequest` | string |  |

## Native endpoint

Through the native Zoho PageSense API, this operation is `POST /portal/:portalName/fulltrackingreports` (base URL `https://pagesense.zoho.com/pagesense/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/individual-stats-report.md) for the provider-specific parameters and requirements.

