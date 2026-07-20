# Invite Candidates By Email with HRBLADE

## Endpoint

- **Method:** `POST`
- **Path:** `/job/invite/create`
- **Base URL:** `https://api.hrblade.com/api`
- **Official documentation:** [Invite Candidates By Email](https://documenter.getpostman.com/view/15055534/TzCFgWPB)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Candidate email address. |
| `job_id` | body | `number` | yes | Job identifier. |
| `name` | body | `string` | yes | Candidate name. |
