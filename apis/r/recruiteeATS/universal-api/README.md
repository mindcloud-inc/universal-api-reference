# <img src="https://images.mindcloud.co/apps/icons/recruitee_1773345532292.png" alt="Recruitee ATS logo" width="28" height="28"> Recruitee ATS: Universal API

Manage candidates, offers, locations, departments, attachments, and hiring pipeline data in Recruitee ATS

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/recruiteeATS/latest
- **Category:** Human Resources / Recruiting
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://recruitee.com
- **Vendor API docs:** https://docs.recruitee.com/reference/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Candidate](actions/get-candidate.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/get-candidate?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Upload Attachment](actions/upload-attachment.md) | POST |  |

### Candidate

| Action | Method | Description |
| --- | --- | --- |
| [Get Candidate](actions/get-candidate.md) | GET |  |
| [List Candidates](actions/list-candidates.md) | GET |  |
| [Search Candidates](actions/search-candidates.md) | GET |  |

### Candidates

| Action | Method | Description |
| --- | --- | --- |
| [Create Candidate](actions/create-candidate.md) | POST |  |
| [Delete Candidate](actions/delete-candidate.md) | DELETE |  |
| [Update Candidate](actions/update-candidate.md) | PUT |  |
| [Update Candidate Custom Fields](actions/update-candidate-custom-fields.md) | PUT |  |
| [Update Candidate CV](actions/update-candidate-cv.md) | PUT |  |

### Department

| Action | Method | Description |
| --- | --- | --- |
| [List Departments](actions/list-departments.md) | GET |  |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [List Locations](actions/list-locations.md) | GET |  |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [List Candidate Notes](actions/list-candidate-notes.md) | GET |  |

### Offer

| Action | Method | Description |
| --- | --- | --- |
| [Get Offer](actions/get-offer.md) | GET |  |
| [List Offers](actions/list-offers.md) | GET |  |

### Offers

| Action | Method | Description |
| --- | --- | --- |
| [Create Offer](actions/create-offer.md) | POST |  |
| [Delete Offer](actions/delete-offer.md) | DELETE |  |

