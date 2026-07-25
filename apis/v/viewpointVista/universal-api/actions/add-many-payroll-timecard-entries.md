# Viewpoint Vista: Add Many Time Batch Entries

Add an array of time batch entries

```
POST https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-many-payroll-timecard-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-many-payroll-timecard-entries" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "items[].data.Co": 1,
  "items[].data.Mth": "2026-05-07T12:00:00.000Z",
  "items[].data.BatchId": 1,
  "items[].data.Employee": 1,
  "items[].data.PostDate": "2026-05-07T12:00:00.000Z",
  "items[].data.Hours": "string",
  "items[].data.TypeDetails": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/add-many-payroll-timecard-entries', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "items[].data.Co": 1,
    "items[].data.Mth": "2026-05-07T12:00:00.000Z",
    "items[].data.BatchId": 1,
    "items[].data.Employee": 1,
    "items[].data.PostDate": "2026-05-07T12:00:00.000Z",
    "items[].data.Hours": "string",
    "items[].data.TypeDetails": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `items[].callerMetadata` | object | no | Use this value to add any properties you may need to reference in case of success and or error. |
| `items[].data.Co` | number | yes | Key to pr/time_batches(Co, Mth, BatchId). |
| `items[].data.TypeDetails.Type` | list<string> | no | Based on the Type chosen - additional details can be specified by adding them as custom fields. |
| `items[]` | array<object> | no | One to 1000 timebatch entry objects. Each item should include the Vista timebatch entry `data` and optional `callerMetadata` |
| `items[].data` | object | no |  |
| `items[].data.Mth` | date | yes | Key to pr/time_batches(Co, Mth, BatchId). Format `YYYY-MM-01` |
| `items[].data.BatchId` | number | yes | Key to pr/time_batches(Co, Mth, BatchId). |
| `items[].data.Employee` | number | yes | Key to pr/employees(PRCo, Employee). |
| `items[].data.PostDate` | date | yes | Date you are entering time for. Format: `YYYY-MM-DD` |
| `items[].data.Hours` | string | yes | Hours. |
| `items[].data.TypeDetails` | object | yes | Provide the object based on the entry type. Options for $.TypeDetails.Type: `J-Job`, `M-Mechanic`, `S-SM Work Order`. |
| `items[].data.PaySeq` | number | no | ( Optional ) If omitted, the first Pay Sequence setup for the Pay Period associated to this batch. |
| `items[].data.PRDept` | string | no | ( Optional ) Key to pr/departments(PRCo, PRDept). If omitted, it will be defaulted based on Vista defaulting logic. |
| `items[].data.InsState` | string | no | Key to pr/states(PRCo, State). Key to pr/insurance_codes(PRCo, InsState, InsCode). Optional. If omitted, will be defaulted based on Vista defaulting logic. Provide null if you want to override the defaulting behavior with no value. |
| `items[].data.TaxState` | string | no | ( Optional ) Key to pr/states(PRCo, State). |
| `items[].data.LocalCode` | string | no | ( Optional ) Key to pr/locals(PRCo, LocalCode). If omitted, will be defaulted based on Vista defaulting logic. Provide `null` if you want to override the defaulting behavior with no value. |
| `items[].data.UnempState` | string | no | ( Optional ) Key to pr/states(PRCo, State). If omitted, will be defaulted based on Vista defaulting logic. |
| `items[].data.InsCode` | string | no | Key to pr/insurance_codes(PRCo, InsState, InsCode). Optional. If omitted, will be defaulted based on Vista defaulting logic. Provide null if you want to override the defaulting behavior with no value. |
| `items[].data.Cert` | list<string> | no | ( Optional ) Should Earnings appear on Certified PR Reports. If omitted, N will be defaulted. |
| `items[].data.Craft` | string | no | Key to pr/crafts(PRCo, Craft). Key to pr/classes(PRCo, Craft, Class). Optional. If omitted, will be defaulted based on Vista defaulting logic. Provide null if you want to override the defaulting behavior with no value. |
| `items[].data.Class` | string | no | Key to pr/classes(PRCo, Craft, Class). Optional. If omitted, will be defaulted based on Vista defaulting logic. Provide null if you want to override the defaulting behavior with no value. |
| `items[].data.StartTime` | string | no | Format 24H:mm (13:24). Optional. If omitted, empty string will be defaulted. This value will only be stored if the StartTime and StopTime are provided. The Hours property will override any calculation based on StartTime, StopTime, and BreakHours. |
| `items[].data.StopTime` | string | no | Format 24H:mm (13:24). Optional. If omitted, empty string will be defaulted. This value will only be stored if the StartTime and StopTime are provided. The Hours property will override any calculation based on StartTime, StopTime, and BreakHours. |
| `items[].data.BreakHours` | string | no | Optional. If omitted, 0 will be defaulted. This value will only be stored if the StartTime and StopTime have also been provided. The Hours property will override any calculation based on StartTime, StopTime, and BreakHours. |
| `items[].data.EarnCode` | number | no | Key to pr/earn_codes(PRCo, EarnCode). Optional. If omitted, will be defaulted based on Vista defaulting logic. |
| `items[].data.Memo` | string | no | ( Optional ) If omitted, null will be defaulted. |
| `items[].data.Shift` | number | no | ( Optional ) If omitted, will be defaulted based on Vista defaulting logic. |
| `items[].data.Rate` | string | no | ( Optional ) If omitted, will be defaulted based on Vista defaulting logic. |
| `items[].data.Amt` | string | no | ( Optional ) Amount. If omitted, it will be defaulted based on Vista defaulting logic. |
| `items[].data.CrewTemplateID` | number | no | ( Optional ) Crew Template ID related to the Vista Web Portal. If omitted, null will be defaulted. |
| `items[].data.__custom_fields` | object | no | Add a property for each user defined values that should be set on the header form as part of this action. |
| `items[].data.__disable_validation` | string | no | Disable Vista validations for properties listed in this field. Accepts multiple values as an array. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `postCacheChanges` | boolean | no | Set true to post cache updates as part of action processing. False if omitted. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Vista API returns.

## Native endpoint

Through the native Viewpoint Vista API, this operation is `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/pr/2/data/time_batch_entries/actions/add_many` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-many-payroll-timecard-entries.md) for the provider-specific parameters and requirements.

