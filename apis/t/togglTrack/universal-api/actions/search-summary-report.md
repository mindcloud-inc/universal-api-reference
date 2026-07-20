# Toggl Track: Search Summary Report

Finds summary report time entries in Toggl Track.

```
GET https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/search-summary-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toggl Track `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/search-summary-report?connectionId=$CONNECTION_ID&workspaceId=1&startDate=string&endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "1",
  "startDate": "string",
  "endDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/search-summary-report?${params}`, {
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
| `workspaceId` | list<number> | yes |  |
| `startDate` | string | yes |  |
| `endDate` | string | yes |  |
| `grouping` | string | no |  |
| `subGrouping` | string | no |  |
| `description` | string | no |  |
| `billable` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "groups": [
        {
          "id": 1,
          "projectColor": "string",
          "projectHexColor": "string",
          "subGroups": [
            {
              "distinguishRates": true,
              "forExport": true,
              "grouping": "string",
              "id": {},
              "localStart": "string",
              "projectColor": "string",
              "projectHexColor": "string",
              "rates": [
                {
                  "billableSeconds": 1,
                  "currency": "string",
                  "hourlyRateInCents": 1
                }
              ],
              "seconds": 1,
              "subGrouping": "string"
            }
          ]
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
| `groups[].id` | number |  |
| `groups[].projectColor` | string |  |
| `groups[].projectHexColor` | string |  |
| `groups[].subGroups[].distinguishRates` | boolean |  |
| `groups[].subGroups[].forExport` | boolean |  |
| `groups[].subGroups[].grouping` | string |  |
| `groups[].subGroups[].id` | object |  |
| `groups[].subGroups[].localStart` | string |  |
| `groups[].subGroups[].projectColor` | string |  |
| `groups[].subGroups[].projectHexColor` | string |  |
| `groups[].subGroups[].rates[].billableSeconds` | number |  |
| `groups[].subGroups[].rates[].currency` | string |  |
| `groups[].subGroups[].rates[].hourlyRateInCents` | number |  |
| `groups[].subGroups[].seconds` | number |  |
| `groups[].subGroups[].subGrouping` | string |  |

## Native endpoint

Through the native Toggl Track API, this operation is `POST /reports/api/v3/workspace/:workspace_id/summary/time_entries` (base URL `https://api.track.toggl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-summary-report.md) for the provider-specific parameters and requirements.

