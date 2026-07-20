# Update Submission with Clappia

Updates an existing submission in Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/submissions/edit`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Update Submission](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Clappia app ID. |
| `submissionId` | body | `string` | yes | Clappia submission ID to edit. |
| `data` | body | `object` | yes | Updated submission payload object keyed by the target app's Clappia field variable names. |
