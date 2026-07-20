# <img src="https://images.mindcloud.co/apps/icons/innform_1775152324434.png" alt="Innform logo" width="28" height="28"> Innform: Universal API

Innform: Manage learners, properties, groups, assignments, courses, and learning paths

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/innform/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.innform.io
- **Vendor API docs:** https://innform.docs.apiary.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/innform/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in Innform. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes a group from Innform. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from Innform. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from Innform. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in Innform. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [List Courses](actions/list-courses.md) | GET | Retrieves courses from Innform. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Create Property](actions/create-property.md) | POST | Creates a new property in Innform. |
| [Delete Property](actions/delete-property.md) | DELETE | Deletes a property from Innform. |
| [Get Property](actions/get-property.md) | GET | Retrieves a property from Innform. |
| [List Properties](actions/list-properties.md) | GET | Retrieves properties from Innform. |
| [Update Property](actions/update-property.md) | PUT | Updates an existing property in Innform. |

### Programs

| Action | Method | Description |
| --- | --- | --- |
| [List Learning Paths](actions/list-learning-paths.md) | GET | Retrieves learning paths from Innform. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Delete User](actions/delete-user.md) | DELETE | Deletes a user from Innform by ID or email. |
| [Freeze User](actions/freeze-user.md) | PUT | Freezes a user in Innform by ID or email. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Innform by ID or email. |
| [Invite User](actions/invite-user.md) | POST | Invites a new user to Innform. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Innform. |
| [Unfreeze User](actions/unfreeze-user.md) | PUT | Unfreezes a user in Innform by ID or email. |
| [Update User](actions/update-user.md) | PUT | Updates a user in Innform by ID or email. |

### Viewer Assignments

| Action | Method | Description |
| --- | --- | --- |
| [Create Assignment](actions/create-assignment.md) | POST | Assigns a training item to a user in Innform. |
| [Delete Assignment](actions/delete-assignment.md) | DELETE | Deletes an assignment from Innform. |
| [List Assignments](actions/list-assignments.md) | GET | Retrieves assignments from Innform. |

