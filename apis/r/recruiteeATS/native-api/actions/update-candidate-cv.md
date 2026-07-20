# Update Candidate CV with Recruitee ATS

## Endpoint

- **Method:** `PATCH`
- **Path:** `/c/:company_id/candidates/:id/update_cv`
- **Base URL:** `https://api.recruitee.com`
- **Official documentation:** [Update Candidate CV](https://docs.recruitee.com/reference/candidatesidupdate_cv)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Candidate ID. |
| `candidate.remote_cv_url` | body | `string` | yes | Public URL to the replacement candidate CV file. |
