# Viewpoint Vista: Update Employee



```
PUT https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/update-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/update-employee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "__key": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/update-employee', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "__key": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `__key` | object | yes | Required employee key. Provide either Key ID or PR Company and Employee. |
| `__key.KeyID` | number | no | Employee record key ID. Use this or the PR Company and Employee pair. |
| `__key.PRCo` | number | no | Payroll company for the employee natural key. Use with Employee when Key ID is not supplied. |
| `__key.Employee` | number | no | Employee number for the natural key. Use with PR Company when Key ID is not supplied. |
| `sortName` | string | no | Optional employee sort name. Maximum 15 characters. |
| `lastName` | string | no | Optional employee last name. Maximum 30 characters. |
| `firstName` | string | no | Optional employee first name. Maximum 30 characters. |
| `midName` | string | no | Optional employee middle name. Maximum 15 characters. |
| `address` | string | no | Optional street address. Maximum 60 characters. |
| `address2` | string | no | Optional second address line. Maximum 60 characters. |
| `city` | string | no | Optional city. Maximum 30 characters. |
| `state` | string | no | Optional state. Must exist in the selected country’s Vista states. |
| `zip` | string | no | Optional postal code. Maximum 12 characters. |
| `country` | string | no | Optional country code. Key to Vista countries. Maximum 2 characters. |
| `email` | string | no | Optional email address. Maximum 255 characters. |
| `phone` | string | no | Optional phone number. Maximum 20 characters. |
| `cellPhone` | string | no | Optional cell phone number. Maximum 20 characters. |
| `notes` | string | no | Optional employee notes. |
| `activeYn` | string | no | Optional status. Allowed values: Y or N. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `suffix` | string | no | Optional name suffix. Maximum 4 characters. |
| `ssn` | string | no | Protected field. Optional Social Security number. Maximum 11 characters. |
| `race` | string | no | Protected field. Optional race code. Maximum 2 characters. |
| `sex` | string | no | Protected field. Optional code: F or M. |
| `birthDate` | string | no | Protected field. Optional date in YYYY-MM-DD format. Example: `2026-09-01`. |
| `hireDate` | string | no | Optional date in YYYY-MM-DD format. Example: `2026-09-01`. |
| `termDate` | string | no | Optional date in YYYY-MM-DD format. Example: `2026-09-01`. |
| `recentRehireDate` | string | no | Optional date in YYYY-MM-DD format. Example: `2026-09-01`. |
| `recentSeparationDate` | string | no | Optional date in YYYY-MM-DD format. Example: `2026-09-01`. |
| `newHireActStartDate` | string | no | Optional date in YYYY-MM-DD format. Example: `2026-09-01`. |
| `newHireActEndDate` | string | no | Optional date in YYYY-MM-DD format. Example: `2026-09-01`. |
| `timesheetRevGroup` | string | no | Optional timesheet reviewer group. Maximum 10 characters. |
| `occupCat` | string | no | Optional occupational category. Maximum 10 characters. |
| `catStatus` | string | no | Optional status: A, J, T, or N. |
| `tradeSeq` | number | no | Optional CHAMP equal-opportunity trade sequence. |
| `nonResAlienYn` | string | no | Protected field. Optional Y/N value. |
| `apVendorGroup` | number | no | Optional AP vendor group. |
| `apVendor` | number | no | Optional AP vendor. |
| `__custom_fields` | object | no | Optional Vista user-defined fields, keyed by field name. |
| `payrollDefaults` | object | no | Optional payroll defaults object. Send documented fields that need changing. |
| `currentJob` | object | no | Optional current job object. Send documented fields that need changing. |
| `standardPay` | object | no | Optional standard pay object. Send documented fields that need changing. |
| `primaryDirectDeposit` | object | no | Optional primary direct deposit object. Send documented fields that need changing. |
| `garnishmentAllocation` | object | no | Optional garnishment allocation object. Send documented fields that need changing. |
| `canadaData` | object | no | Optional Canada-specific payroll data object. |
| `australiaData` | object | no | Optional Australia-specific payroll data object. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Vista API returns.

## Native endpoint

Through the native Viewpoint Vista API, this operation is `POST v1/direct/subscribers/{{credentials.subscriberCode}}/vista/pr/2/data/employees/actions/change` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-employee.md) for the provider-specific parameters and requirements.

