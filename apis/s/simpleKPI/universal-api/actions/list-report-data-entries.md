# SimpleKPI: List Report Data Entries

Retrieves report data entries from SimpleKPI.

```
GET https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/list-report-data-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleKPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/list-report-data-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/list-report-data-entries?${params}`, {
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
| `fromDate` | string | no | Optional report start date. |
| `toDate` | string | no | Optional report end date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actual": 1,
      "direction": "string",
      "directionName": "Ava Chen",
      "entryDate": "string",
      "hasTarget": true,
      "isPercentage": true,
      "itemId": 1,
      "itemName": "Ava Chen",
      "kpiDescription": "string",
      "kpiId": 1,
      "kpiName": "Ava Chen",
      "labelFormat": "string",
      "notes": "string",
      "period": "string",
      "periodId": "string",
      "target": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actual` | number |  |
| `direction` | string |  |
| `directionName` | string |  |
| `entryDate` | string |  |
| `hasTarget` | boolean |  |
| `isPercentage` | boolean |  |
| `itemId` | number |  |
| `itemName` | string |  |
| `kpiDescription` | string |  |
| `kpiId` | number |  |
| `kpiName` | string |  |
| `labelFormat` | string |  |
| `notes` | string |  |
| `period` | string |  |
| `periodId` | string |  |
| `target` | number |  |

## Native endpoint

Through the native SimpleKPI API, this operation is `GET reports/AllDataEntries` (base URL `https://{{credentials.subdomain}}.simplekpi.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-report-data-entries.md) for the provider-specific parameters and requirements.

