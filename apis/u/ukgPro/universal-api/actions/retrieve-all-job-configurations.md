# UKG Pro: Retrieve All Job Configurations



```
GET https://connect.mindcloud.co/v1/universal/ukgPro/latest/actions/retrieve-all-job-configurations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UKG Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ukgPro/latest/actions/retrieve-all-job-configurations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ukgPro/latest/actions/retrieve-all-job-configurations?${params}`, {
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
      "autoAllocate": "string",
      "clockCode": "string",
      "companyCode": "string",
      "companyGLSegment": "string",
      "companyID": "string",
      "companyName": "Ava Chen",
      "dateInJob": "2026-05-07T12:00:00.000Z",
      "dateLastPayDatePaid": "2026-05-07T12:00:00.000Z",
      "dateLastWorked": "2026-05-07T12:00:00.000Z",
      "dateOfBenefitSeniority": "2026-05-07T12:00:00.000Z",
      "dateOfEarlyRetirement": "2026-05-07T12:00:00.000Z",
      "dateOfLocalUnion": "2026-05-07T12:00:00.000Z",
      "dateOfNationalUnion": "2026-05-07T12:00:00.000Z",
      "dateOfRetirement": "2026-05-07T12:00:00.000Z",
      "dateOfSeniority": "2026-05-07T12:00:00.000Z",
      "dateOfSuspension": "2026-05-07T12:00:00.000Z",
      "dateOfTermination": "2026-05-07T12:00:00.000Z",
      "datePaidThru": "2026-05-07T12:00:00.000Z",
      "dateTimeChanged": "2026-05-07T12:00:00.000Z",
      "dateTimeCreated": "2026-05-07T12:00:00.000Z",
      "deductionGroupCode": "string",
      "earningGroupCode": "string",
      "employeeID": "string",
      "employeeNumber": "string",
      "employeeStatusCode": "string",
      "employeeTypeCode": "string",
      "fullTimeOrPartTimeCode": "string",
      "hireSource": "string",
      "isAutoAllocated": "string",
      "isAutopaid": "string",
      "isMultipleJob": "string",
      "jobChangeReasonCode": "string",
      "jobDescription": "string",
      "jobGroupCode": "string",
      "jobTitle": "string",
      "languageCode": "string",
      "lastHireDate": "2026-05-07T12:00:00.000Z",
      "leaveReasonCode": "string",
      "locationGLSegment": "string",
      "mailstop": "string",
      "okToRehire": "string",
      "orgLevel1Code": "string",
      "orgLevel2Code": "string",
      "orgLevel3Code": "string",
      "orgLevel4Code": "string",
      "originalHireDate": "2026-05-07T12:00:00.000Z",
      "payGroup": "string",
      "payGroupDescription": "string",
      "payPeriod": "string",
      "plannedLeaveReason": "string",
      "positionCode": "string",
      "primaryJobCode": "string",
      "primaryProjectCode": "string",
      "primaryWorkLocationCode": "string",
      "salaryOrHourly": "https://example.com",
      "scheduledAnnualHrs": 1,
      "scheduledFTE": 1,
      "scheduledWorkHrs": 1,
      "shift": "string",
      "shiftGroup": "string",
      "statusStartDate": "2026-05-07T12:00:00.000Z",
      "supervisorCOID": "string",
      "supervisorCompanyCode": "string",
      "supervisorEmployeeNumber": "string",
      "supervisorFirstName": "Ava",
      "supervisorID": "string",
      "supervisorLastName": "Chen",
      "terminationReasonDescription": "string",
      "termReason": "string",
      "termType": "string",
      "timeclockID": "string",
      "unionLocal": "string",
      "unionNational": "string",
      "weeklyHours": 1,
      "workPhoneCountry": "string",
      "workPhoneExtension": "string",
      "workPhoneNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoAllocate` | string |  |
| `clockCode` | string |  |
| `companyCode` | string |  |
| `companyGLSegment` | string |  |
| `companyID` | string |  |
| `companyName` | string |  |
| `dateInJob` | date |  |
| `dateLastPayDatePaid` | date |  |
| `dateLastWorked` | date |  |
| `dateOfBenefitSeniority` | date |  |
| `dateOfEarlyRetirement` | date |  |
| `dateOfLocalUnion` | date |  |
| `dateOfNationalUnion` | date |  |
| `dateOfRetirement` | date |  |
| `dateOfSeniority` | date |  |
| `dateOfSuspension` | date |  |
| `dateOfTermination` | date |  |
| `datePaidThru` | date |  |
| `dateTimeChanged` | date |  |
| `dateTimeCreated` | date |  |
| `deductionGroupCode` | string |  |
| `earningGroupCode` | string |  |
| `employeeID` | string |  |
| `employeeNumber` | string |  |
| `employeeStatusCode` | string |  |
| `employeeTypeCode` | string |  |
| `fullTimeOrPartTimeCode` | string |  |
| `hireSource` | string |  |
| `isAutoAllocated` | string |  |
| `isAutopaid` | string |  |
| `isMultipleJob` | string |  |
| `jobChangeReasonCode` | string |  |
| `jobDescription` | string |  |
| `jobGroupCode` | string |  |
| `jobTitle` | string |  |
| `languageCode` | string |  |
| `lastHireDate` | date |  |
| `leaveReasonCode` | string |  |
| `locationGLSegment` | string |  |
| `mailstop` | string |  |
| `okToRehire` | string |  |
| `orgLevel1Code` | string |  |
| `orgLevel2Code` | string |  |
| `orgLevel3Code` | string |  |
| `orgLevel4Code` | string |  |
| `originalHireDate` | date |  |
| `payGroup` | string |  |
| `payGroupDescription` | string |  |
| `payPeriod` | string |  |
| `plannedLeaveReason` | string |  |
| `positionCode` | string |  |
| `primaryJobCode` | string |  |
| `primaryProjectCode` | string |  |
| `primaryWorkLocationCode` | string |  |
| `salaryOrHourly` | string |  |
| `scheduledAnnualHrs` | number |  |
| `scheduledFTE` | number |  |
| `scheduledWorkHrs` | number |  |
| `shift` | string |  |
| `shiftGroup` | string |  |
| `statusStartDate` | date |  |
| `supervisorCOID` | string |  |
| `supervisorCompanyCode` | string |  |
| `supervisorEmployeeNumber` | string |  |
| `supervisorFirstName` | string |  |
| `supervisorID` | string |  |
| `supervisorLastName` | string |  |
| `terminationReasonDescription` | string |  |
| `termReason` | string |  |
| `termType` | string |  |
| `timeclockID` | string |  |
| `unionLocal` | string |  |
| `unionNational` | string |  |
| `weeklyHours` | number |  |
| `workPhoneCountry` | string |  |
| `workPhoneExtension` | string |  |
| `workPhoneNumber` | string |  |

## Native endpoint

Through the native UKG Pro API, this operation is `GET configuration/v1/jobs` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-all-job-configurations.md) for the provider-specific parameters and requirements.

