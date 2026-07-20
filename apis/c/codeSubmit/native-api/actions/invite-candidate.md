# Invite Candidate with CodeSubmit

## Endpoint

- **Method:** `POST`
- **Path:** `/api/external/candidates`
- **Base URL:** `https://app.codesubmit.io`
- **Official documentation:** [Invite Candidate](https://www.codesubmit.io/integrations/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `due_at` | body | `string` | no | Assessment due date/time |
| `email` | body | `string` | no | Candidate email address |
| `first_name` | body | `string` | no | Candidate first name |
| `last_name` | body | `string` | no | Candidate last name |
| `test_id` | body | `string` | no | Assessment identifier |
| `time_limit` | body | `number` | no | Time limit in minutes |
