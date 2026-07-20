# Create Job with HRBLADE

## Endpoint

- **Method:** `POST`
- **Path:** `/job/create`
- **Base URL:** `https://api.hrblade.com/api`
- **Official documentation:** [Create Job](https://documenter.getpostman.com/view/15055534/TzCFgWPB)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | body | `string` | yes | Company identifier for the job. |
| `description` | body | `string` | no | Job description text. |
| `for_follow_up` | body | `boolean` | yes | Whether this is a follow-up job posting. |
| `name` | body | `string` | yes | Job title. |
| `questions[0]` | body | `string` | no | Stringified question object, e.g. {"type":"VIDEO","question":"...","time":"00:01:00","sorting":0}. |
