# Create Submission with Clappia

Creates a new submission in Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/submissions/create`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Create Submission](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Clappia app ID. |
| `requestingUserEmailAddress` | body | `string` | yes | Email address of the Clappia user on whose behalf the submission is created. |
| `data` | body | `object` | yes | Submission payload object keyed by the target app's Clappia field variable names. |
