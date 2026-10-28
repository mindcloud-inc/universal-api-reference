# UKG Ready: Create Time Punches



```
POST https://connect.mindcloud.co/v1/universal/uKGReady/latest/actions/create-time-punches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UKG Ready `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uKGReady/latest/actions/create-time-punches" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "punches[].timestamp": "2026-05-07T12:00:00.000Z",
  "punches[].raw_type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uKGReady/latest/actions/create-time-punches', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "punches[].timestamp": "2026-05-07T12:00:00.000Z",
    "punches[].raw_type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyID` | string | no |  |
| `punches[].cost_centers[].index` | number | no |  |
| `punches[].cost_centers[].value.id` | number | no |  |
| `punches[].employee` | object | no |  |
| `punches[].employee.account_id` | number | no |  |
| `punches[]` | array<object> | no |  |
| `punches[].cost_centers[].value` | object | no |  |
| `punches[].employee.badge_id` | string | no |  |
| `punches[].ip` | string | no |  |
| `punches[].timestamp` | date | yes |  |
| `punches[].timestamp_type` | list<string> | no |  |
| `punches[].raw_type` | list<string> | yes |  |
| `punches[].latitude` | number | no |  |
| `punches[].longitude` | number | no |  |
| `punches[].cost_centers[]` | array<object> | no |  |
| `punches[].device_id` | string | no |  |
| `punches[].terminal_id` | number | no |  |
| `punches[].status` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "employee": {
        "accountId": 1
      },
      "endDate": "string",
      "startDate": "string",
      "timeEntries": [
        {
          "approvalStatus": "string",
          "calcTotal": 1,
          "costCenters": [
            {
              "index": 1,
              "value": {
                "id": 1
              }
            }
          ],
          "date": "string",
          "id": 1,
          "isCalc": true,
          "isRaw": true,
          "total": 1,
          "type": "string"
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
| `employee.accountId` | number |  |
| `endDate` | string |  |
| `startDate` | string |  |
| `timeEntries[].approvalStatus` | string |  |
| `timeEntries[].calcTotal` | number |  |
| `timeEntries[].costCenters[].index` | number |  |
| `timeEntries[].costCenters[].value.id` | number |  |
| `timeEntries[].date` | string |  |
| `timeEntries[].id` | number |  |
| `timeEntries[].isCalc` | boolean |  |
| `timeEntries[].isRaw` | boolean |  |
| `timeEntries[].total` | number |  |
| `timeEntries[].type` | string |  |

## Native endpoint

Through the native UKG Ready API, this operation is `POST /v2/companies/:cid/time-punches/collection` (base URL `https://{{credentials.hostname}}/ta/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-time-punches.md) for the provider-specific parameters and requirements.

