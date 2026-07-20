# <img src="https://images.mindcloud.co/apps/icons/class-do_1775063742041.png" alt="ClassDo logo" width="28" height="28"> ClassDo: Universal API

ClassDo GraphQL API integration for rooms, members, invitations, and recording workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/classDo/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.classdo.com
- **Vendor API docs:** https://developer.classdo.com/schema/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Rooms](actions/list-rooms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/classDo/latest/actions/list-rooms?connectionId=$CONNECTION_ID&query=query%20ListRooms%20%7B%20viewer%20%7B%20rooms(input%3A%20%7B%20first%3A%2020%2C%20orderBy%3A%20createdAt_DESC%20%7D)%20%7B%20edges%20%7B%20node%20%7B%20id%20name%20%7D%20%7D%20%7D%20%7D%20%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Add Room Members](actions/add-room-members.md) | POST | Adds members to a room in ClassDo. |
| [Create Room](actions/create-room.md) | POST | Creates a new room in ClassDo. |
| [Delete Room](actions/delete-room.md) | DELETE | Deletes an existing room from ClassDo. |
| [Delete Room Member](actions/delete-room-member.md) | DELETE | Deletes an existing room member from ClassDo. |
| [Get Viewer](actions/get-viewer.md) | GET | Retrieves the current viewer from ClassDo. |
| [List Organization Member Roles](actions/list-organization-member-roles.md) | GET | Retrieves organization member roles from ClassDo. |
| [List Organization Members](actions/list-organization-members.md) | GET | Retrieves organization member records from ClassDo. |
| [List Rooms](actions/list-rooms.md) | GET | Retrieves a list of rooms from ClassDo. |
| [Lock Room](actions/lock-room.md) | PUT | Updates a room to locked in ClassDo. |
| [Search Recording Videos](actions/search-recording-videos.md) | GET | Finds recording videos in ClassDo by search criteria. |
| [Send Invitation](actions/send-invitation.md) | POST | Creates a new invitation in ClassDo. |
| [Start Recording](actions/start-recording.md) | PUT | Updates a recording to started in ClassDo. |
| [Stop Recording](actions/stop-recording.md) | PUT | Updates a recording to stopped in ClassDo. |
| [Unlock Room](actions/unlock-room.md) | PUT | Updates a room to unlocked in ClassDo. |
| [Update Organization Member](actions/update-organization-member.md) | PUT | Updates an organization member in ClassDo. |

