# <img src="https://images.mindcloud.co/apps/icons/f-track_1776278770935.png" alt="FTrack logo" width="28" height="28"> FTrack: Universal API

ftrack is a production tracking and asset management platform for creative teams. This app connects to the ftrack API for querying and mutating workspace data through the documented /api operation surface.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fTrack/latest
- **Category:** Productivity / Project Management
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ftrack.com
- **Vendor API docs:** https://developer.ftrack.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Query Server Information](actions/query-server-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/query-server-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Check Permissions](actions/check-permissions.md) | GET | Checks permissions in FTrack for an entity. |
| [Complete Multipart Upload](actions/complete-multipart-upload.md) | POST | Completes a multipart upload in FTrack. |
| [Convert Entity Type](actions/convert-entity-type.md) | PUT | Converts an entity type in FTrack. |
| [Create Entity](actions/create-entity.md) | POST | Creates an entity in FTrack. |
| [CSV Import Delayed Job](actions/csv-import-delayed-job.md) | POST | Creates a CSV import delayed job in FTrack. |
| [Delete Delayed Job](actions/delete-delayed-job.md) | DELETE | Deletes a delayed job from FTrack. |
| [Delete Entity](actions/delete-entity.md) | DELETE | Deletes an entity from FTrack. |
| [Encode Media](actions/encode-media.md) | POST | Creates a media encoding job in FTrack. |
| [Export Review Session Feedback](actions/export-review-session-feedback.md) | POST | Creates a review session feedback export in FTrack. |
| [Generate Signed URL](actions/generate-signed-url.md) | GET | Generates a signed URL in FTrack. |
| [Get Storage Usage](actions/get-storage-usage.md) | GET | Retrieves storage usage from FTrack. |
| [Get Upload Metadata](actions/get-upload-metadata.md) | GET | Retrieves upload metadata from FTrack. |
| [Parse Query](actions/parse-query.md) | GET | Parses a query expression in FTrack. |
| [Query Entities](actions/query-entities.md) | GET | Retrieves entities from FTrack using an expression. |
| [Query Schemas](actions/query-schemas.md) | GET | Retrieves entity schemas from FTrack. |
| [Query Server Information](actions/query-server-information.md) | GET | Retrieves server information from FTrack. |
| [Search Entities](actions/search-entities.md) | GET | Searches entities in FTrack by terms and entity type. |
| [Send Review Session Invite](actions/send-review-session-invite.md) | POST | Creates a review session invite in FTrack. |
| [Update Entity](actions/update-entity.md) | PUT | Updates an entity in FTrack. |

