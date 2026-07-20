# <img src="https://images.mindcloud.co/apps/icons/othership_1775760469255.png" alt="Othership logo" width="28" height="28"> Othership: Universal API

Manage workplace bookings, visitors, and employee scheduling

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/othership/latest
- **Category:** Productivity / Scheduling
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://othership.com
- **Vendor API docs:** https://knowledge.othership.com/workplace-software-faq-admins?hsLang=en

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/othership/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in Othership. |
| [Get Group](actions/get-group.md) | GET | Retrieves a specific group from Othership. |
| [List Groups](actions/list-groups.md) | GET | Retrieves group records from Othership SCIM. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in Othership. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in Othership. |
| [Deactivate User](actions/deactivate-user.md) | PUT | Deactivates an existing user in Othership. |
| [Get User](actions/get-user.md) | GET | Retrieves a specific user from Othership. |
| [List Users](actions/list-users.md) | GET | Retrieves user records from Othership SCIM. |
| [Reactivate User](actions/reactivate-user.md) | PUT | Reactivates an existing user in Othership. |
| [Update User](actions/update-user.md) | PUT | Updates an existing user in Othership. |

