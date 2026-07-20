# <img src="https://images.mindcloud.co/apps/icons/id-mo-s8fl7k-logos_1776968481631.jpeg" alt="Sumsub logo" width="28" height="28"> Sumsub: Universal API

Digital identity verification and compliance platform for KYC, AML screening, fraud prevention, transaction monitoring, and business verification.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sumsub/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sumsub.com
- **Vendor API docs:** https://docs.sumsub.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Verification Levels](actions/list-verification-levels.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/list-verification-levels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Applicant

| Action | Method | Description |
| --- | --- | --- |
| [Get Applicant-Facing Consents](actions/get-applicant-facing-consents.md) | GET |  |
| [Get Applicant Review History](actions/get-applicant-review-history.md) | GET |  |
| [List Applicant Actions](actions/list-applicant-actions.md) | GET |  |
| [List Applicant Notes](actions/list-applicant-notes.md) | GET |  |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Get Document Image Metadata](actions/get-document-image-metadata.md) | GET |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Add Applicant Note](actions/add-applicant-note.md) | POST |  |
| [Add Applicant Tags](actions/add-applicant-tags.md) | POST |  |
| [Approve Applicant](actions/approve-applicant.md) | PUT |  |
| [Blocklist Applicant](actions/blocklist-applicant.md) | PUT |  |
| [Create Applicant](actions/create-applicant.md) | POST |  |
| [Edit Applicant Note](actions/edit-applicant-note.md) | PUT |  |
| [Generate Access Token](actions/generate-access-token.md) | POST |  |
| [Get Applicant Data](actions/get-applicant-data.md) | GET |  |
| [Get Applicant Data By External User ID](actions/get-applicant-data-by-external-user-id.md) | GET |  |
| [Get Applicant Review Status](actions/get-applicant-review-status.md) | GET |  |
| [Import Applicant From Archive](actions/import-applicant-from-archive.md) | POST |  |
| [List Verification Levels](actions/list-verification-levels.md) | GET |  |

