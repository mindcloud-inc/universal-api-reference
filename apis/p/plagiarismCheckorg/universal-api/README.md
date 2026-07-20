# <img src="https://images.mindcloud.co/apps/icons/plagiarism-checkorg_1775064839589.png" alt="PlagiarismCheck.org logo" width="28" height="28"> PlagiarismCheck.org: Universal API

Check plagiarism, detect AI content, and retrieve detailed reports

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/plagiarismCheckorg/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://plagiarismcheck.org
- **Vendor API docs:** https://plagiarismcheck.org/for-developers/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate Plagiarism Text Before Submit](actions/validate-plagiarism-text-before-submit.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/validate-plagiarism-text-before-submit?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Delete Organization Check](actions/delete-organization-check.md) | DELETE |  |
| [Get AI Check Report](actions/get-ai-check-report.md) | GET |  |
| [Get AI Check Status](actions/get-ai-check-status.md) | GET |  |
| [Get Organization Check Status](actions/get-organization-check-status.md) | GET |  |
| [Get Organization Report](actions/get-organization-report.md) | GET |  |
| [Get Plagiarism Check Status](actions/get-plagiarism-check-status.md) | GET |  |
| [Get Plagiarism Report](actions/get-plagiarism-report.md) | GET |  |
| [Submit AI Check For B2B Group](actions/submit-ai-check-for-b2b-group.md) | POST |  |
| [Submit AI Check From File](actions/submit-ai-check-from-file.md) | POST |  |
| [Submit AI Check From Text](actions/submit-ai-check-from-text.md) | POST |  |
| [Submit Organization Check With Custom Author](actions/submit-organization-check-with-custom-author.md) | POST |  |
| [Submit Organization File Check](actions/submit-organization-file-check.md) | POST |  |
| [Submit Organization Plagiarism Check](actions/submit-organization-plagiarism-check.md) | POST |  |
| [Submit Plagiarism Check](actions/submit-plagiarism-check.md) | POST |  |
| [Validate Plagiarism Text Before Submit](actions/validate-plagiarism-text-before-submit.md) | GET |  |

