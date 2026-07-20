# <img src="https://images.mindcloud.co/apps/icons/papyrs_1775567619338.png" alt="Papyrs logo" width="28" height="28"> Papyrs: Universal API

Papyrs is a company intranet and document management platform. This wrapper lets agents list pages, read page content, manage page widgets, search content, access people records, and post to activity feeds from a Papyrs workspace.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/papyrs/latest
- **Category:** Content & Files / Storage
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://papyrs.com/
- **Vendor API docs:** https://papyrs.com/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Pages](actions/list-pages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/list-pages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Attachments

| Action | Method | Description |
| --- | --- | --- |
| [Create Attachment Widget](actions/create-attachment-widget.md) | POST |  |
| [Delete Attachment Widget](actions/delete-attachment-widget.md) | DELETE |  |
| [Get Attachment Widget](actions/get-attachment-widget.md) | GET |  |
| [Update Attachment Widget](actions/update-attachment-widget.md) | PUT |  |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Post To Activity Stream](actions/post-to-activity-stream.md) | POST |  |
| [Post To Page Discussion](actions/post-to-page-discussion.md) | POST |  |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Create Heading Widget](actions/create-heading-widget.md) | POST |  |
| [Create Page](actions/create-page.md) | POST |  |
| [Create Text Box Widget](actions/create-text-box-widget.md) | POST |  |
| [Delete Heading Widget](actions/delete-heading-widget.md) | DELETE |  |
| [Delete Page](actions/delete-page.md) | DELETE |  |
| [Delete Text Box Widget](actions/delete-text-box-widget.md) | DELETE |  |
| [Get Heading Widget](actions/get-heading-widget.md) | GET |  |
| [Get Page](actions/get-page.md) | GET |  |
| [Get Text Box Widget](actions/get-text-box-widget.md) | GET |  |
| [List Page Records](actions/list-page-records.md) | GET |  |
| [List Pages](actions/list-pages.md) | GET |  |
| [Update Heading Widget](actions/update-heading-widget.md) | PUT |  |
| [Update Text Box Widget](actions/update-text-box-widget.md) | PUT |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Search Results](actions/search-results.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Delete User](actions/delete-user.md) | DELETE |  |
| [List People](actions/list-people.md) | GET |  |

