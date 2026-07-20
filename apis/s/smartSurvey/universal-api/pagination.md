# SmartSurvey Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model SmartSurvey expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSurvey/latest/actions/list-survey-exports?connectionId=$CONNECTION_ID&limit=25&offset=0&surveyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## SmartSurvey actions that support pagination

- [List Survey Exports](actions/list-survey-exports.md)
- [List Survey Folders](actions/list-survey-folders.md)
- [List Survey Invitation Responses](actions/list-survey-invitation-responses.md)
- [List Survey Invitations](actions/list-survey-invitations.md)
- [List Survey Responses](actions/list-survey-responses.md)
- [List Survey Tracking Links](actions/list-survey-tracking-links.md)
- [List Surveys](actions/list-surveys.md)
