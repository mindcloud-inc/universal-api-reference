# SmartSurvey Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format SmartSurvey expects, and each action page lists the fields available to sort.

## SmartSurvey actions that support sorting

- [List Survey Exports](actions/list-survey-exports.md)
- [List Survey Folders](actions/list-survey-folders.md)
- [List Survey Invitation Responses](actions/list-survey-invitation-responses.md)
- [List Survey Invitations](actions/list-survey-invitations.md)
- [List Survey Responses](actions/list-survey-responses.md)
- [List Survey Tracking Links](actions/list-survey-tracking-links.md)
- [List Surveys](actions/list-surveys.md)
