# <img src="https://images.mindcloud.co/apps/icons/class-marker_1774278683514.png" alt="ClassMarker logo" width="28" height="28"> ClassMarker: Universal API

Online testing and quiz platform for retrieving exam results, managing access lists, and maintaining question banks and categories.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/classMarker/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.classmarker.com
- **Vendor API docs:** https://www.classmarker.com/online-testing/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Available Groups Links and Exams](actions/list-available-groups-links-and-exams.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/classMarker/latest/actions/list-available-groups-links-and-exams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Access List

| Action | Method | Description |
| --- | --- | --- |
| [Add Access Codes](actions/add-access-codes.md) | PUT |  |
| [Remove Access Codes](actions/remove-access-codes.md) | PUT |  |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | POST |  |
| [List Categories](actions/list-categories.md) | GET |  |
| [Update Category](actions/update-category.md) | PUT |  |

### Exam Inventory

| Action | Method | Description |
| --- | --- | --- |
| [List Available Groups Links and Exams](actions/list-available-groups-links-and-exams.md) | GET |  |

### Parent Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Parent Category](actions/create-parent-category.md) | POST |  |
| [Update Parent Category](actions/update-parent-category.md) | PUT |  |

### Question

| Action | Method | Description |
| --- | --- | --- |
| [Create Question](actions/create-question.md) | POST |  |
| [Get Question](actions/get-question.md) | GET |  |
| [List Questions](actions/list-questions.md) | GET |  |
| [Update Question](actions/update-question.md) | PUT |  |

### Result

| Action | Method | Description |
| --- | --- | --- |
| [List Recent Results for All Groups](actions/list-recent-results-for-all-groups.md) | GET |  |
| [List Recent Results for All Links](actions/list-recent-results-for-all-links.md) | GET |  |
| [List Recent Results for Specific Group Exam](actions/list-recent-results-for-specific-group-exam.md) | GET |  |
| [List Recent Results for Specific Link Exam](actions/list-recent-results-for-specific-link-exam.md) | GET |  |

