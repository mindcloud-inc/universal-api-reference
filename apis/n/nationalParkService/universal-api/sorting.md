# National Park Service Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format National Park Service expects, and each action page lists the fields available to sort.

## National Park Service actions that support sorting

- [List Activities](actions/list-activities.md)
- [List Campgrounds](actions/list-campgrounds.md)
- [List Fees And Passes](actions/list-fees-and-passes.md)
- [List Lesson Plans](actions/list-lesson-plans.md)
- [List News Releases](actions/list-news-releases.md)
- [List Parks](actions/list-parks.md)
- [List Things To Do](actions/list-things-to-do.md)
- [List Topics](actions/list-topics.md)
- [List Tours](actions/list-tours.md)
- [List Visitor Centers](actions/list-visitor-centers.md)
