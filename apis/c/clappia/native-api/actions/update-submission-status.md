# Update Submission Status with Clappia

Updates an existing submission status in Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/submissions/updateStatus`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Update Submission Status](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Clappia app ID. |
| `submissionId` | body | `string` | yes | Clappia submission ID whose status should be updated. |
| `status` | body | `object` | yes | Status object containing the target status name and optional comments. |
