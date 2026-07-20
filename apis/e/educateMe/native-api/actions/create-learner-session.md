# Create Learner Session with EducateMe

Creates a learner session in EducateMe.

## Endpoint

- **Method:** `POST`
- **Path:** `/students/:email/sessions`
- **Base URL:** `https://api.educate-me.co`
- **Official documentation:** [Create Learner Session](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#95f11204f20e4a9eb5aa6e5b7f31ec6e)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | Learner email. |
| `expireInDays` | body | `number` | no | Number of days the token will be active. Default is 100. |
