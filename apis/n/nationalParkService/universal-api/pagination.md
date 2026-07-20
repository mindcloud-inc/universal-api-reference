# National Park Service Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model National Park Service expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nationalParkService/latest/actions/list-activities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## National Park Service actions that support pagination

- [List Activities](actions/list-activities.md)
- [List Alerts](actions/list-alerts.md)
- [List Amenities](actions/list-amenities.md)
- [List Articles](actions/list-articles.md)
- [List Audio](actions/list-audio.md)
- [List Campgrounds](actions/list-campgrounds.md)
- [List Fees And Passes](actions/list-fees-and-passes.md)
- [List Galleries](actions/list-galleries.md)
- [List Gallery Assets](actions/list-gallery-assets.md)
- [List Lesson Plans](actions/list-lesson-plans.md)
- [List News Releases](actions/list-news-releases.md)
- [List Parking Lots](actions/list-parking-lots.md)
- [List Parks](actions/list-parks.md)
- [List Passport Stamp Locations](actions/list-passport-stamp-locations.md)
- [List People](actions/list-people.md)
- [List Places](actions/list-places.md)
- [List Things To Do](actions/list-things-to-do.md)
- [List Topics](actions/list-topics.md)
- [List Tours](actions/list-tours.md)
- [List Videos](actions/list-videos.md)
- [List Visitor Centers](actions/list-visitor-centers.md)
- [List Webcams](actions/list-webcams.md)
