# <img src="https://images.mindcloud.co/apps/icons/favicon-32x32_1775240177695.png" alt="FileCloud logo" width="28" height="28"> FileCloud: Universal API

Enterprise file storage and content management with SCIM-based user and group provisioning.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fileCloud/latest
- **Category:** Content & Files / Storage
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.filecloud.com
- **Vendor API docs:** https://fcapi-v1.filecloud.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Resource Types](actions/list-resource-types.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fileCloud/latest/actions/list-resource-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in FileCloud. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from FileCloud. |
| [Get Group by ID](actions/get-group-by-id.md) | GET | Retrieves a group from FileCloud by ID. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from FileCloud. |
| [Update Group](actions/update-group.md) | PUT | Replaces an existing group in FileCloud. |

### Resource Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Resource Type by Name](actions/get-resource-type-by-name.md) | GET | Retrieves a resource type from FileCloud by name. |
| [List Resource Types](actions/list-resource-types.md) | GET | Retrieves resource types from FileCloud. |

### Schema

| Action | Method | Description |
| --- | --- | --- |
| [List Schemas](actions/list-schemas.md) | GET | Retrieves schemas from FileCloud. |

### Service Provider Configuration

| Action | Method | Description |
| --- | --- | --- |
| [Get Service Provider Configuration](actions/get-service-provider-configuration.md) | GET | Retrieves service provider configuration from FileCloud. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User by ID](actions/get-user-by-id.md) | GET | Retrieves a user from FileCloud by ID. |
| [List Users](actions/list-users.md) | GET | Retrieves users from FileCloud. |
| [Patch User](actions/patch-user.md) | PUT | Partially updates an existing user in FileCloud. |
| [Update User](actions/update-user.md) | PUT | Replaces an existing user in FileCloud. |

