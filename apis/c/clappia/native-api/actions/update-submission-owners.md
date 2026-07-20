# Update Submission Owners with Clappia

Updates submission owners for an existing Clappia submission.

## Endpoint

- **Method:** `POST`
- **Path:** `/submissions/updateSubmissionOwners`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Update Submission Owners](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Clappia app ID. |
| `submissionId` | body | `string` | yes | Clappia submission ID whose owners should be updated. |
| `emailIds[]` | body | `array<string>` | yes | Array of Clappia owner email addresses to assign to the submission. |
