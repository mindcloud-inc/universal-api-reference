# Congress.gov Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Congress.gov expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/list-amendment-actions?connectionId=$CONNECTION_ID&limit=25&offset=0&congress=118&amendmentType=samdt&amendmentNumber=2137" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Congress.gov actions that support pagination

- [List Amendment Actions](actions/list-amendment-actions.md)
- [List Amendment Cosponsors](actions/list-amendment-cosponsors.md)
- [List Amendments](actions/list-amendments.md)
- [List Bill Actions](actions/list-bill-actions.md)
- [List Bill Amendments](actions/list-bill-amendments.md)
- [List Bill Committees](actions/list-bill-committees.md)
- [List Bill Cosponsors](actions/list-bill-cosponsors.md)
- [List Bill Subjects](actions/list-bill-subjects.md)
- [List Bill Summaries](actions/list-bill-summaries.md)
- [List Bill Text Versions](actions/list-bill-text-versions.md)
- [List Bill Titles](actions/list-bill-titles.md)
- [List Bills](actions/list-bills.md)
- [List Bills By Congress](actions/list-bills-by-congress.md)
- [List Bills By Congress And Type](actions/list-bills-by-congress-and-type.md)
- [List Committee Bills](actions/list-committee-bills.md)
- [List Committee Meetings](actions/list-committee-meetings.md)
- [List Committee Prints](actions/list-committee-prints.md)
- [List Committee Reports](actions/list-committee-reports.md)
- [List Committees](actions/list-committees.md)
- [List Congresses](actions/list-congresses.md)
- [List Hearings](actions/list-hearings.md)
- [List Laws By Congress](actions/list-laws-by-congress.md)
- [List Laws By Congress And Type](actions/list-laws-by-congress-and-type.md)
- [List Member Cosponsored Legislation](actions/list-member-cosponsored-legislation.md)
- [List Member Sponsored Legislation](actions/list-member-sponsored-legislation.md)
- [List Members](actions/list-members.md)
- [List Members By Congress](actions/list-members-by-congress.md)
- [List Related Bills](actions/list-related-bills.md)
- [List Summaries](actions/list-summaries.md)
- [List Summaries By Congress](actions/list-summaries-by-congress.md)
- [List Summaries By Congress And Bill Type](actions/list-summaries-by-congress-and-bill-type.md)
