# Add Many Time Batch Entries with Viewpoint Vista

Add an array of time batch entries

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/{subscriberCode}/vista/pr/2/data/time_batch_entries/actions/add_many`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Add Many Time Batch Entries](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistapr2datatime_batch_entriesactionsadd_many)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `items[].callerMetadata` | body | `object` | no | Use this value to add any properties you may need to reference in case of success and or error. |
| `items[].data.Co` | body | `number` | yes | Key to pr/time_batches(Co, Mth, BatchId). |
| `items[].data.TypeDetails.Job.JCCo` | body | `number` | no | — |
| `items[].data.TypeDetails.Type` | body | `list<string>` | no | Based on the Type chosen - additional details can be specified by adding them as custom fields. |
| `postCacheChanges` | body | `boolean` | no | Set true to post cache updates as part of action processing. False if omitted. |
| `items[]` | body | `array<object>` | no | One to 1000 timebatch entry objects. Each item should include the Vista timebatch entry `data` and optional `callerMetadata` |
| `items[].data` | body | `object` | no | — |
| `items[].data.Mth` | body | `date` | yes | Key to pr/time_batches(Co, Mth, BatchId).  Format `YYYY-MM-01` |
| `items[].data.TypeDetails.Job` | body | `object` | no | — |
| `items[].data.TypeDetails.Job.Job` | body | `string` | no | — |
| `items[].data.BatchId` | body | `number` | yes | Key to pr/time_batches(Co, Mth, BatchId). |
| `items[].data.TypeDetails.Job.Phase` | body | `string` | no | — |
| `items[].data.Employee` | body | `number` | yes | Key to pr/employees(PRCo, Employee). |
| `items[].data.PostDate` | body | `date` | yes | Date you are entering time for.  Format: `YYYY-MM-DD` |
| `items[].data.Hours` | body | `string` | yes | Hours. |
| `items[].data.TypeDetails` | body | `object` | yes | Provide the object based on the entry type.  Options for $.TypeDetails.Type: `J-Job`, `M-Mechanic`, `S-SM Work Order`. |
| `items[].data.PaySeq` | body | `number` | no | ( Optional ) If omitted, the first Pay Sequence setup for the Pay Period associated to this batch. |
| `items[].data.PRDept` | body | `string` | no | ( Optional ) Key to pr/departments(PRCo, PRDept). If omitted, it will be defaulted based on Vista defaulting logic. Maximum length: 10. |
| `items[].data.InsState` | body | `string` | no | Key to pr/states(PRCo, State). Key to pr/insurance_codes(PRCo, InsState, InsCode). Optional. If omitted, will be defaulted based on Vista defaulting logic. Provide null if you want to override the defaulting behavior with no value. |
| `items[].data.TaxState` | body | `string` | no | ( Optional ) Key to pr/states(PRCo, State). Maximum length: 4. |
| `items[].data.LocalCode` | body | `string` | no | ( Optional ) Key to pr/locals(PRCo, LocalCode).  If omitted, will be defaulted based on Vista defaulting logic. Provide `null` if you want to override the defaulting behavior with no value. |
| `items[].data.UnempState` | body | `string` | no | ( Optional ) Key to pr/states(PRCo, State).  If omitted, will be defaulted based on Vista defaulting logic. Maximum length: 4. |
| `items[].data.InsCode` | body | `string` | no | Key to pr/insurance_codes(PRCo, InsState, InsCode). Optional. If omitted, will be defaulted based on Vista defaulting logic. Provide null if you want to override the defaulting behavior with no value. |
| `items[].data.Cert` | body | `list<string>` | no | ( Optional ) Should Earnings appear on Certified PR Reports.  If omitted, N will be defaulted. |
| `items[].data.Craft` | body | `string` | no | Key to pr/crafts(PRCo, Craft). Key to pr/classes(PRCo, Craft, Class). Optional. If omitted, will be defaulted based on Vista defaulting logic. Provide null if you want to override the defaulting behavior with no value. |
| `items[].data.Class` | body | `string` | no | Key to pr/classes(PRCo, Craft, Class). Optional. If omitted, will be defaulted based on Vista defaulting logic. Provide null if you want to override the defaulting behavior with no value. |
| `items[].data.StartTime` | body | `string` | no | Format 24H:mm (13:24). Optional. If omitted, empty string will be defaulted. This value will only be stored if the StartTime and StopTime are provided. The Hours property will override any calculation based on StartTime, StopTime, and BreakHours. |
| `items[].data.StopTime` | body | `string` | no | Format 24H:mm (13:24). Optional. If omitted, empty string will be defaulted. This value will only be stored if the StartTime and StopTime are provided. The Hours property will override any calculation based on StartTime, StopTime, and BreakHours. |
| `items[].data.BreakHours` | body | `string` | no | Optional. If omitted, 0 will be defaulted. This value will only be stored if the StartTime and StopTime have also been provided. The Hours property will override any calculation based on StartTime, StopTime, and BreakHours. |
| `items[].data.EarnCode` | body | `number` | no | Key to pr/earn_codes(PRCo, EarnCode). Optional. If omitted, will be defaulted based on Vista defaulting logic. |
| `items[].data.Memo` | body | `string` | no | ( Optional ) If omitted, null will be defaulted. |
| `items[].data.Shift` | body | `number` | no | ( Optional ) If omitted, will be defaulted based on Vista defaulting logic. |
| `items[].data.Rate` | body | `string` | no | ( Optional ) If omitted, will be defaulted based on Vista defaulting logic. |
| `items[].data.Amt` | body | `string` | no | ( Optional ) Amount. If omitted, it will be defaulted based on Vista defaulting logic. |
| `items[].data.CrewTemplateID` | body | `number` | no | ( Optional ) Crew Template ID related to the Vista Web Portal. If omitted, null will be defaulted. |
| `items[].data.__custom_fields` | body | `object` | no | Add a property for each user defined values that should be set on the header form as part of this action. |
| `items[].data.__disable_validation` | body | `string` | no | Disable Vista validations for properties listed in this field. Send multiple values as a array. |
