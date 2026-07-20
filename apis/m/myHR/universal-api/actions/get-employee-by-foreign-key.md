# MyHR: Get Employee By Foreign Key



```
GET https://connect.mindcloud.co/v1/universal/myHR/latest/actions/get-employee-by-foreign-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myHR/latest/actions/get-employee-by-foreign-key?connectionId=$CONNECTION_ID&employeeForeignKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employeeForeignKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myHR/latest/actions/get-employee-by-foreign-key?${params}`, {
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
| `employeeForeignKey` | string | yes | Employee foreign key used to resolve the @ endpoint header. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateCreation": "string",
      "dateLastAction": "string",
      "dateLastUpdate": "string",
      "employeeAddress": {
        "city": "string",
        "countryCode": "string",
        "dateCreation": "string",
        "dateLastAction": "string",
        "dateLastUpdate": "string",
        "number": "string",
        "object": "string",
        "pid": "string",
        "street": "string",
        "zipcode": "string"
      },
      "employeeJob": {
        "companyJobDepartment": {
          "dateCreation": "string",
          "dateLastAction": "string",
          "label": "string",
          "object": "string",
          "pid": "string"
        },
        "companyJobDivision": {
          "dateCreation": "string",
          "dateLastAction": "string",
          "label": "string",
          "object": "string",
          "pid": "string"
        },
        "companyJobTitle": {
          "dateCreation": "string",
          "dateLastAction": "string",
          "label": "string",
          "object": "string",
          "pid": "string"
        },
        "dateCreation": "string",
        "dateLastAction": "string",
        "dateLastUpdate": "string",
        "effectiveDate": "string",
        "object": "string",
        "pid": "string",
        "supervisor": {
          "dateCreation": "string",
          "dateLastAction": "string",
          "dateLastUpdate": "string",
          "EmployeeAddress": "string",
          "EmployeeEmploymentStatus": "string",
          "EmployeeJob": "string",
          "EmployeeStatus": "string",
          "hireDate": "string",
          "internalNumber": "string",
          "object": "string",
          "Person": "string",
          "pid": "string",
          "seniorityDate": "string",
          "sosecNumber": "string"
        }
      },
      "employeeStatus": {
        "dateCreation": "string",
        "dateLastAction": "string",
        "object": "string",
        "pid": "string",
        "tag": {}
      },
      "foreignKey": "string",
      "hireDate": "string",
      "internalNumber": "string",
      "object": "string",
      "person": {
        "birthDate": "string",
        "dateCreation": "string",
        "dateLastAction": "string",
        "dateLastUpdate": "string",
        "firstName": "Ava",
        "gender": "string",
        "hasSelfService": true,
        "language": "string",
        "maritalStatus": "string",
        "object": "string",
        "phoneWork": "string",
        "phoneWorkCountryCode": "string",
        "phoneWorkFormatted": "string",
        "phoneWorkMobile": "string",
        "phoneWorkMobileCountryCode": "string",
        "phoneWorkMobileFormatted": "string",
        "pid": "string",
        "usualName": "Ava Chen",
        "workEmail": "ava@example.com"
      },
      "pid": "string",
      "seniorityDate": "string",
      "status": {
        "dateCreation": "string",
        "dateLastAction": "string",
        "dateLastUpdate": "string",
        "effectiveDate": "string",
        "fullTimeEquivalent": "string",
        "object": "string",
        "pid": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreation` | string |  |
| `dateLastAction` | string |  |
| `dateLastUpdate` | string |  |
| `employeeAddress.city` | string |  |
| `employeeAddress.countryCode` | string |  |
| `employeeAddress.dateCreation` | string |  |
| `employeeAddress.dateLastAction` | string |  |
| `employeeAddress.dateLastUpdate` | string |  |
| `employeeAddress.number` | string |  |
| `employeeAddress.object` | string |  |
| `employeeAddress.pid` | string |  |
| `employeeAddress.street` | string |  |
| `employeeAddress.zipcode` | string |  |
| `employeeJob.companyJobDepartment.dateCreation` | string |  |
| `employeeJob.companyJobDepartment.dateLastAction` | string |  |
| `employeeJob.companyJobDepartment.label` | string |  |
| `employeeJob.companyJobDepartment.object` | string |  |
| `employeeJob.companyJobDepartment.pid` | string |  |
| `employeeJob.companyJobDivision.dateCreation` | string |  |
| `employeeJob.companyJobDivision.dateLastAction` | string |  |
| `employeeJob.companyJobDivision.label` | string |  |
| `employeeJob.companyJobDivision.object` | string |  |
| `employeeJob.companyJobDivision.pid` | string |  |
| `employeeJob.companyJobTitle.dateCreation` | string |  |
| `employeeJob.companyJobTitle.dateLastAction` | string |  |
| `employeeJob.companyJobTitle.label` | string |  |
| `employeeJob.companyJobTitle.object` | string |  |
| `employeeJob.companyJobTitle.pid` | string |  |
| `employeeJob.dateCreation` | string |  |
| `employeeJob.dateLastAction` | string |  |
| `employeeJob.dateLastUpdate` | string |  |
| `employeeJob.effectiveDate` | string |  |
| `employeeJob.object` | string |  |
| `employeeJob.pid` | string |  |
| `employeeJob.supervisor.dateCreation` | string |  |
| `employeeJob.supervisor.dateLastAction` | string |  |
| `employeeJob.supervisor.dateLastUpdate` | string |  |
| `employeeJob.supervisor.EmployeeAddress` | string |  |
| `employeeJob.supervisor.EmployeeEmploymentStatus` | string |  |
| `employeeJob.supervisor.EmployeeJob` | string |  |
| `employeeJob.supervisor.EmployeeStatus` | string |  |
| `employeeJob.supervisor.hireDate` | string |  |
| `employeeJob.supervisor.internalNumber` | string |  |
| `employeeJob.supervisor.object` | string |  |
| `employeeJob.supervisor.Person` | string |  |
| `employeeJob.supervisor.pid` | string |  |
| `employeeJob.supervisor.seniorityDate` | string |  |
| `employeeJob.supervisor.sosecNumber` | string |  |
| `employeeStatus.dateCreation` | string |  |
| `employeeStatus.dateLastAction` | string |  |
| `employeeStatus.object` | string |  |
| `employeeStatus.pid` | string |  |
| `employeeStatus.tag` | object |  |
| `foreignKey` | string |  |
| `hireDate` | string |  |
| `internalNumber` | string |  |
| `object` | string |  |
| `person.birthDate` | string |  |
| `person.dateCreation` | string |  |
| `person.dateLastAction` | string |  |
| `person.dateLastUpdate` | string |  |
| `person.firstName` | string |  |
| `person.gender` | string |  |
| `person.hasSelfService` | boolean |  |
| `person.language` | string |  |
| `person.maritalStatus` | string |  |
| `person.object` | string |  |
| `person.phoneWork` | string |  |
| `person.phoneWorkCountryCode` | string |  |
| `person.phoneWorkFormatted` | string |  |
| `person.phoneWorkMobile` | string |  |
| `person.phoneWorkMobileCountryCode` | string |  |
| `person.phoneWorkMobileFormatted` | string |  |
| `person.pid` | string |  |
| `person.usualName` | string |  |
| `person.workEmail` | string |  |
| `pid` | string |  |
| `seniorityDate` | string |  |
| `status.dateCreation` | string |  |
| `status.dateLastAction` | string |  |
| `status.dateLastUpdate` | string |  |
| `status.effectiveDate` | string |  |
| `status.fullTimeEquivalent` | string |  |
| `status.object` | string |  |
| `status.pid` | string |  |

## Native endpoint

Through the native MyHR API, this operation is `GET /employees/@` (base URL `https://mindcloud.myhr.lu/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employee-by-foreign-key.md) for the provider-specific parameters and requirements.

