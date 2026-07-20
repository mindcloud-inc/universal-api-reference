# TimeLive: List Employees

Retrieves active employee records from TimeLive.

```
GET https://connect.mindcloud.co/v1/universal/timeLive/latest/actions/list-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimeLive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeLive/latest/actions/list-employees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeLive/latest/actions/list-employees?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "AccountDepartmentId": 1,
      "AccountEmployeeId": 1,
      "AccountEmployeeType": "string",
      "AccountHolidayTypeId": "string",
      "AccountLocation": "string",
      "AccountLocationId": 1,
      "AccountRoleId": 1,
      "AccountTimeOffPolicy": "string",
      "AccountTimeOffPolicyId": "string",
      "AccountWorkingDayTypeId": "string",
      "AddressLine1": "string",
      "AddressLine2": "string",
      "AllowedAccessFromIP": "string",
      "BillingType": "string",
      "City": "string",
      "CreatedOn": "string",
      "CustomField1": "string",
      "CustomField10": "string",
      "CustomField11": "string",
      "CustomField12": "string",
      "CustomField13": "string",
      "CustomField14": "string",
      "CustomField15": "string",
      "CustomField2": "string",
      "CustomField3": "string",
      "CustomField4": "string",
      "CustomField5": "string",
      "CustomField6": "string",
      "CustomField7": "string",
      "CustomField8": "string",
      "CustomField9": "string",
      "Department": "string",
      "DepartmentName": "Ava Chen",
      "EMailAddress": "ava@example.com",
      "EmployeeCode": "string",
      "EmployeeCountryId": 1,
      "EmployeeManagerId": "string",
      "EmployeePayTypeId": "string",
      "EmployeeTimeZoneId": 1,
      "FirstName": "Ava",
      "HiredDate": "string",
      "HomePhoneNo": "string",
      "IsDisabled": "string",
      "IsForcePasswordChange": "string",
      "IsShowEmployeeProfilePicture": "string",
      "JobTitle": "string",
      "LastName": "Chen",
      "MobilePhoneNo": "string",
      "ModifiedOn": "string",
      "Role": "string",
      "State": "string",
      "StatusId": 1,
      "TerminationDate": "string",
      "TimeOffApprovalTypeId": "string",
      "UserInterfaceLanguage": "string",
      "Username": "Ava Chen",
      "WorkPhoneNo": "string",
      "Zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AccountDepartmentId` | number |  |
| `AccountEmployeeId` | number |  |
| `AccountEmployeeType` | string |  |
| `AccountHolidayTypeId` | string |  |
| `AccountLocation` | string |  |
| `AccountLocationId` | number |  |
| `AccountRoleId` | number |  |
| `AccountTimeOffPolicy` | string |  |
| `AccountTimeOffPolicyId` | string |  |
| `AccountWorkingDayTypeId` | string |  |
| `AddressLine1` | string |  |
| `AddressLine2` | string |  |
| `AllowedAccessFromIP` | string |  |
| `BillingType` | string |  |
| `City` | string |  |
| `CreatedOn` | string |  |
| `CustomField1` | string |  |
| `CustomField10` | string |  |
| `CustomField11` | string |  |
| `CustomField12` | string |  |
| `CustomField13` | string |  |
| `CustomField14` | string |  |
| `CustomField15` | string |  |
| `CustomField2` | string |  |
| `CustomField3` | string |  |
| `CustomField4` | string |  |
| `CustomField5` | string |  |
| `CustomField6` | string |  |
| `CustomField7` | string |  |
| `CustomField8` | string |  |
| `CustomField9` | string |  |
| `Department` | string |  |
| `DepartmentName` | string |  |
| `EMailAddress` | string |  |
| `EmployeeCode` | string |  |
| `EmployeeCountryId` | number |  |
| `EmployeeManagerId` | string |  |
| `EmployeePayTypeId` | string |  |
| `EmployeeTimeZoneId` | number |  |
| `FirstName` | string |  |
| `HiredDate` | string |  |
| `HomePhoneNo` | string |  |
| `IsDisabled` | string |  |
| `IsForcePasswordChange` | string |  |
| `IsShowEmployeeProfilePicture` | string |  |
| `JobTitle` | string |  |
| `LastName` | string |  |
| `MobilePhoneNo` | string |  |
| `ModifiedOn` | string |  |
| `Role` | string |  |
| `State` | string |  |
| `StatusId` | number |  |
| `TerminationDate` | string |  |
| `TimeOffApprovalTypeId` | string |  |
| `UserInterfaceLanguage` | string |  |
| `Username` | string |  |
| `WorkPhoneNo` | string |  |
| `Zip` | string |  |

## Native endpoint

Through the native TimeLive API, this operation is `GET /Employees` (base URL `https://mindcloudtl.livetecs.com/classic/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employees.md) for the provider-specific parameters and requirements.

