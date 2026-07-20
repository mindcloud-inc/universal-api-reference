# Create Rock with Ninety.io

Creates a new rock in Ninety.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/rocks`
- **Base URL:** `https://api.public.ninety.io`
- **Official documentation:** [Create Rock](https://api.public.ninety.io/v1/swagger)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | body | `list<string>` | yes | The Id of the team the Rock belongs to |
| `title` | body | `string` | yes | The title of the Rock |
| `dueDate` | body | `date` | yes | The due date of the Rock (ISO 8601) |
| `statusCode` | body | `list<string>` | yes | The status of the Rock: OFF_TRACK, ON_TRACK, DONE, or CANCELED Accepted values: `CANCELED`, `DONE`, `OFF_TRACK`, `ON_TRACK`. |
| `levelCode` | body | `list<string>` | yes | The level of the Rock: USER, COMPANY_AND_DEPARTMENT, COMPANY, or DEPARTMENT Accepted values: `COMPANY`, `COMPANY_AND_DEPARTMENT`, `DEPARTMENT`, `USER`. |
| `quarter` | body | `list<string>` | yes | The quarter associated with the Rock: Q1, Q2, Q3, Q4, or None Accepted values: `None`, `Q1`, `Q2`, `Q3`, `Q4`. |
| `description` | body | `string` | no | The description of the Rock |
| `additionalTeamIds[]` | body | `list<string>` | no | Additional team Ids that can also view this Rock Send multiple values as a array. |
| `futureScope` | body | `list<string>` | no | The future scope of the Rock: Current, Next, Later, or Future Accepted values: `Current`, `Future`, `Later`, `Next`. |
| `rockQuarterYearDueDate` | body | `date` | no | The quarter-aligned year due date of the Rock (ISO 8601) |
| `addCreatorToFollowersList` | body | `boolean` | no | When true, the authenticated user is added to the Rock's followers list |
