# List Course Availabilities with CoachAccountable

Retrieves course availabilities from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [List Course Availabilities](https://www.coachaccountable.com/APIDocs#Course.getAvailabilitiesForCourse)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CourseID` | body | `number` | yes | The ID of the Course for which Client Availabilities are to be gotten. |
| `includeUsed` | body | `boolean` | no | Include Course Availabilities which have already been used. |
