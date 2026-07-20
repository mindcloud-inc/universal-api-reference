# Get Submissions Excel with Clappia

Retrieves a submissions export file from Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/submissions/getSubmissionsExcel`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Get Submissions Excel](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Clappia app ID. |
| `requestingUserEmailAddress` | body | `string` | yes | Email address of the Clappia user on whose behalf the export should run. |
| `pageSize` | body | `number` | no | Maximum number of submissions to include per page while preparing the export. |
| `filters` | body | `object` | no | Optional Clappia filters object for narrowing the exported submissions. |
