# Update Candidate with Recruitee ATS

## Endpoint

- **Method:** `PATCH`
- **Path:** `/c/:company_id/candidates/:id`
- **Base URL:** `https://api.recruitee.com`
- **Official documentation:** [Update Candidate](https://docs.recruitee.com/reference/candidatesid-patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Candidate ID. |
| `candidate.name` | body | `string` | no | Candidate name. |
| `candidate.remote_cv_url` | body | `string` | no | Public URL to the candidate CV file. |
| `candidate.emails` | body | `list<string>` | no | Candidate email addresses. |
| `candidate.phones` | body | `list<string>` | no | Candidate phone numbers. |
| `candidate.social_links` | body | `list<string>` | no | Candidate social profile URLs. |
| `candidate.links` | body | `list<string>` | no | Additional candidate links. |
| `candidate.cover_letter` | body | `string` | no | Candidate cover letter text. |
