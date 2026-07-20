# TimeLive Universal API Examples

These examples use the MindCloud API key and TimeLive connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Employees

Retrieves active employee records from TimeLive.

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

Example response:

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

See the full [List Employees action reference](actions/list-employees.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/timeLive/latest/actions/list-employees).
