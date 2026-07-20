# <img src="https://images.mindcloud.co/apps/icons/goto-human_1775824565268.png" alt="gotoHuman logo" width="28" height="28"> gotoHuman: Universal API

Request, review, and manage human approvals for AI workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gotoHuman/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.gotohuman.com
- **Vendor API docs:** https://docs.gotohuman.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Review Forms](actions/list-review-forms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gotoHuman/latest/actions/list-review-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Upload Files](actions/upload-files.md) | POST | Uploads files to gotoHuman. |

### Form Submissions

| Action | Method | Description |
| --- | --- | --- |
| [Create Review Request](actions/create-review-request.md) | POST | Creates a new review request in gotoHuman. |
| [Fetch Responses](actions/fetch-responses.md) | GET | Retrieves past review responses from gotoHuman. |
| [Query Responses](actions/query-responses.md) | GET |  |
| [Update Review Request](actions/update-review-request.md) | PUT | Updates an existing review request in gotoHuman. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Get Form Schema](actions/get-form-schema.md) | GET | Retrieves a review form schema from gotoHuman. |
| [List Review Forms](actions/list-review-forms.md) | GET | Retrieves review templates from gotoHuman. |

