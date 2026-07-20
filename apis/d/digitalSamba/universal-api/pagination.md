# Digital Samba Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Digital Samba expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digitalSamba/latest/actions/get-all-participants?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Digital Samba actions that support pagination

- [Get all participants](actions/get-all-participants.md)
- [Get all room participants](actions/get-all-room-participants.md)
- [Get all room sessions](actions/get-all-room-sessions.md)
- [Get all session participants](actions/get-all-session-participants.md)
- [Get all sessions](actions/get-all-sessions.md)
- [Get all team recordings](actions/get-all-team-recordings.md)
- [Get all team rooms](actions/get-all-team-rooms.md)
- [Get archived team recordings](actions/get-archived-team-recordings.md)
- [Get available libraries for the team](actions/get-available-libraries-for-the-team.md)
- [Get available library files](actions/get-available-library-files.md)
- [Get available roles for the team](actions/get-available-roles-for-the-team.md)
- [Get chat messages](actions/get-chat-messages.md)
- [Get questions and answers](actions/get-questions-and-answers.md)
- [Get room transcripts](actions/get-room-transcripts.md)
- [Get rooms with live participants count](actions/get-rooms-with-live-participants-count.md)
- [Get rooms with live participants data](actions/get-rooms-with-live-participants-data.md)
- [Get session transcripts](actions/get-session-transcripts.md)
- [Get webhooks for the team](actions/get-webhooks-for-the-team.md)
