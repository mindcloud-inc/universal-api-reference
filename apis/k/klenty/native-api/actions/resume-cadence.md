# Resume Cadence with Klenty

Resumes cadence for a prospect in Klenty.

## Endpoint

- **Method:** `POST`
- **Path:** `/cadences/resume`
- **Base URL:** `https://api.klenty.com/apis/v1/user/{username}`
- **Official documentation:** [Resume Cadence](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_e44dfcb398)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Email` | body | `string` | yes | Prospect email to resume cadence for. |
