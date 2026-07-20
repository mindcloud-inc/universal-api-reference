# Digital Samba Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format Digital Samba expects, and each action page lists the fields available to sort.

## Digital Samba actions that support sorting

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
