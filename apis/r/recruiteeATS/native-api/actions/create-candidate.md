# Create Candidate with Recruitee ATS

## Endpoint

- **Method:** `POST`
- **Path:** `/c/:company_id/candidates`
- **Base URL:** `https://api.recruitee.com`
- **Official documentation:** [Create Candidate](https://docs.recruitee.com/reference/candidates-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `candidate.name` | body | `string` | yes | Candidate name. |
| `candidate.remote_cv_url` | body | `string` | no | Public URL to the candidate CV file. |
| `candidate.emails` | body | `list<string>` | no | Candidate email addresses. |
| `candidate.phones` | body | `list<string>` | no | Candidate phone numbers. |
| `candidate.social_links` | body | `list<string>` | no | Candidate social profile URLs. |
| `candidate.links` | body | `list<string>` | no | Additional candidate links. |
| `candidate.cover_letter` | body | `string` | no | Candidate cover letter text. |
| `candidate.sources` | body | `list<string>` | no | Source tags to assign to the candidate. |
| `offers` | body | `list<number>` | no | Offer IDs to assign to the candidate. |
