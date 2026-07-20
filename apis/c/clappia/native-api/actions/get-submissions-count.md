# Get Submissions Count with Clappia

Retrieves the matching submissions count from Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/submissions/getSubmissionsCount`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Get Submissions Count](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Clappia app ID. |
| `requestingUserEmailAddress` | body | `string` | yes | Email address of the Clappia user on whose behalf the count should run. |
| `filters` | body | `object` | no | Optional Clappia filters object for narrowing the submission count. |
