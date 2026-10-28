# UKG Ready: Delete Time Entry



```
DELETE https://connect.mindcloud.co/v1/universal/uKGReady/latest/actions/delete-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UKG Ready `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/uKGReady/latest/actions/delete-time-entry?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uKGReady/latest/actions/delete-time-entry?${params}`, {
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
| `companyID` | string | no |  |
| `time_entry_id` | string | no |  |

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

Through the native UKG Ready API, this operation is `DELETE /v2/companies/:cid/time-entries/:time_entry_id` (base URL `https://{{credentials.hostname}}/ta/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-time-entry.md) for the provider-specific parameters and requirements.

