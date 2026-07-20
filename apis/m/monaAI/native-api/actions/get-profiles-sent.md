# Get Profiles Sent with Mona AI

Retrieves sent profiles from Mona AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/matching/getProfilesSent`
- **Base URL:** `https://api.mona-ai.cloud`
- **Official documentation:** [Get Profiles Sent](https://api-docs.mona-ai.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endDate` | body | `date` | no | End date for the profiles-sent range. |
| `limit` | body | `number` | no | Maximum profiles-sent records to return. |
| `startDate` | body | `date` | no | Start date for the profiles-sent range. |
