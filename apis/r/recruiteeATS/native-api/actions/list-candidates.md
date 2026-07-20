# List Candidates with Recruitee ATS

## Endpoint

- **Method:** `GET`
- **Path:** `/c/:company_id/candidates`
- **Base URL:** `https://api.recruitee.com`
- **Official documentation:** [List Candidates](https://docs.recruitee.com/reference/candidates-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Specifies the number of candidates to retrieve. |
| `offset` | query | `number` | no | Skip number of candidates from the beginning. |
| `created_after` | query | `string` | no | Show only candidates created after the given date-time. |
| `disqualified` | query | `boolean` | no | Show only candidates disqualified in at least one job. |
| `qualified` | query | `boolean` | no | Show only candidates qualified in at least one job. |
| `ids` | query | `string` | no | Comma-separated list of candidate IDs. |
| `offer_id` | query | `number` | no | Filter by offer. |
| `query` | query | `string` | no | Search query for candidate name or offer. |
| `sort` | query | `string` | no | Sorting option. |
| `with_messages` | query | `boolean` | no | Show only candidates with messages. |
| `with_my_messages` | query | `boolean` | no | Show only candidates with messages sent by the current admin. |
