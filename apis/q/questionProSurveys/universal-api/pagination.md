# QuestionPro Surveys Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model QuestionPro Surveys expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-all-users-from-organization?connectionId=$CONNECTION_ID&limit=25&offset=0&organizationId=6137544" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## QuestionPro Surveys actions that support pagination

- [Get All Users from Organization](actions/get-all-users-from-organization.md)
- [Get Answers](actions/get-answers.md)
- [Get Folder Surveys](actions/get-folder-surveys.md)
- [Get Folders](actions/get-folders.md)
- [Get Images](actions/get-images.md)
- [Get Questions](actions/get-questions.md)
- [Get Responses](actions/get-responses.md)
- [Get Survey Blocks](actions/get-survey-blocks.md)
- [Get User Surveys](actions/get-user-surveys.md)
