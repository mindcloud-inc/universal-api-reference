# List Courses with Edusign

Retrieves courses from Edusign.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/course`
- **Base URL:** `https://ext.edusign.fr`
- **Official documentation:** [List Courses](https://developers.edusign.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `string` | no | Query param for pagination, starts at page "0" and displays 40 courses per page |
| `start` | query | `string` | no | Filter courses based on the course start date (format YYYY-MM-DD, ISO 8601) |
| `end` | query | `string` | no | Filter courses based on the course end date (format YYYY-MM-DD, ISO 8601). The difference between the start and end date must be 90 days maximum |
| `filters` | query | `string` | no | Filters must be separated by a comma ",". List of available filters :  <br /> - locked : Retrieve all the locked courses <br /> - unlocked : Retrieve all the unlocked courses <br /> - absencessent : Retrieve all the absences send courses <br /> - absencesnotsent : Retrieve all the absences not send courses |
| `groupId` | query | `string` | no | Filter courses based on an array of groupIds to retrieve courses for specific groups Multiple groupIds can be provided, separated by commas (e.g., ?groupId=123,456,789). |
| `studentId` | query | `string` | no | Filter courses based on an array of studentIds to retrieve courses for specific students. Multiple studentIds can be provided, separated by commas (e.g., ?studentId=123,456,789). |
| `professorId` | query | `string` | no | Filter courses based on an array of professorIds to retrieve courses for specific professors. Multiple professorIds can be provided, separated by commas (e.g., ?studentId=123,456,789). |
| `trainingId` | query | `string` | no | Filter courses based on an array of trainingIds. Multiple trainingIds can be provided, separated by commas (e.g., ?trainingId=training123,training456). |
| `classroom` | query | `string` | no | Filter courses based on the classroom. |
| `creatorId` | query | `string` | no | Filter courses based on creatorId to retrieve courses for specific creatorId |
| `courseName` | query | `string` | no | Filter courses based on courseName to retrieve courses for specific courseName |
| `dateCreated` | query | `string` | no | Filter courses based on an array of two dates (start and end) (e.g., ?dateCreated=2024-08-01, 2024-08-02). |
| `infoStudents` | query | `string` | no | Returns detailed student information for the first course only. Values: "true" or "false" (default) Example: ?infoStudents=true Description: If "true", includes student details (first name, last name, email). If "false", only student states are returned. |
| `dateUpdated` | query | `string` | no | Filter courses based on an array of two dates (start and end) (e.g., ?dateUpdated=2024-08-01, 2024-08-02). |
| `professorSignature` | query | `string` | no | Filter courses based on professor's signature (true or false) |
