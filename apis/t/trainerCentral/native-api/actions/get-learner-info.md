# Get Learner Info with TrainerCentral

Retrieves learner info from signup forms in TrainerCentral.

## Endpoint

- **Method:** `GET`
- **Path:** `/fetchuserdetails.json`
- **Base URL:** `{academyUrl}/api/v4/{orgId}`
- **Official documentation:** [Get Learner Info](https://help.trainercentral.com/portal/en/kb/articles/get-learner-info)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | The learner email address to fetch. |
| `fetchSignupData` | query | `boolean` | yes | Set true to include signup form field data with the master fields. |
