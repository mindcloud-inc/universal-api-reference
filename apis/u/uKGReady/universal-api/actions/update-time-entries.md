# UKG Ready: Update Time Entries



```
PUT https://connect.mindcloud.co/v1/universal/uKGReady/latest/actions/update-time-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UKG Ready `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/uKGReady/latest/actions/update-time-entries" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uKGReady/latest/actions/update-time-entries', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyID` | string | no |  |
| `time_entry_sets[].employee` | object | no |  |
| `time_entry_sets[].employee.account_id` | number | no |  |
| `time_entry_sets[].time_entries[].cost_centers[].index` | number | no |  |
| `time_entry_sets[].time_entries[].cost_centers[].value.id` | number | no |  |
| `time_entry_sets[].time_entries[].pay_category.id` | number | no |  |
| `time_entry_sets[].time_entries[].premium_shift.id` | number | no |  |
| `time_entry_sets[].time_entries[].time_off.id` | number | no |  |
| `time_entry_sets[]` | array<object> | no |  |
| `time_entry_sets[].time_entries[].cost_centers[]` | array<object> | no |  |
| `time_entry_sets[].time_entries[].cost_centers[].value` | object | no |  |
| `time_entry_sets[].time_entries[].type` | list<string> | no |  |
| `partial_update` | boolean | no | Use to update entries within the specified time range, instead of replacing them. |
| `time_entry_sets[].end_date` | date | no | Date needs to be in the format yyyy-mm-dd within the 1900-12-31 and 2079-06-05 date range |
| `time_entry_sets[].start_date` | date | no | Date needs to be in the format yyyy-mm-dd within the 1900-12-31 and 2079-06-05 date range |
| `time_entry_sets[].time_entries[].date` | date | no | Date needs to be in the format yyyy-mm-dd within the 1900-12-31 and 2079-06-05 date range |
| `time_entry_sets[].time_entries[].start_time` | date | no | (date-time) |
| `time_entry_sets[].time_entries[]` | array<object> | no |  |
| `time_entry_sets[].time_entries[].end_time` | date | no | (date-time) |
| `time_entry_sets[].time_entries[].total` | number | no |  |
| `time_entry_sets[].time_entries[].time_off` | object | no |  |
| `time_entry_sets[].time_entries[].pay_category` | object | no |  |
| `time_entry_sets[].time_entries[].premium_shift` | object | no |  |
| `time_entry_sets[].time_entries[].piecework` | number | no |  |
| `time_entry_sets[].time_entries[].amount` | number | no |  |
| `time_entry_sets[].time_entries[].from` | date | no | Date needs to be in the format yyyy-mm-dd within the 1900-12-31 and 2079-06-05 date range |
| `time_entry_sets[].time_entries[].to` | date | no | Date needs to be in the format yyyy-mm-dd within the 1900-12-31 and 2079-06-05 date range |

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

Through the native UKG Ready API, this operation is `PUT /v2/companies/:cid/time-entries/collection` (base URL `https://{{credentials.hostname}}/ta/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-time-entries.md) for the provider-specific parameters and requirements.

