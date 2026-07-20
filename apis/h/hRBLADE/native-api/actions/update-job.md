# Update Job with HRBLADE

## Endpoint

- **Method:** `POST`
- **Path:** `/job/update`
- **Base URL:** `https://api.hrblade.com/api`
- **Official documentation:** [Update Job](https://documenter.getpostman.com/view/15055534/TzCFgWPB)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | body | `number` | no | Company identifier for the job. |
| `description` | body | `string` | no | Job description text. |
| `for_follow_up` | body | `boolean` | yes | Whether this is a follow-up job posting. |
| `job_id` | body | `number` | yes | Job identifier. |
| `name` | body | `string` | no | Job title. |
| `questions[0]` | body | `string` | no | Stringified question object, e.g. {"type":"VIDEO","question":"...","time":"00:01:00","sorting":0}. |
