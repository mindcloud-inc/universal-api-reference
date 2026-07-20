# Innform: Native API Reference

A consolidated summary of Innform's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://innform.docs.apiary.io/
- **API base URL:** `https://api.innform.io/v1`

## Authentication

### API Key

Use your Innform API key to access the Innform Public API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.innform.io/en/articles/5664688-does-innform-offer-a-public-api)

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Assignment](actions/create-assignment.md) | `POST /assignments` | [docs](https://innform.docs.apiary.io/) |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://innform.docs.apiary.io/) |
| [Create Property](actions/create-property.md) | `POST /properties` | [docs](https://innform.docs.apiary.io/) |
| [Delete Assignment](actions/delete-assignment.md) | `DELETE /assignments/{id}` | [docs](https://innform.docs.apiary.io/) |
| [Delete Group](actions/delete-group.md) | `DELETE /groups/{id}` | [docs](https://innform.docs.apiary.io/) |
| [Delete Property](actions/delete-property.md) | `DELETE /properties/{id}` | [docs](https://innform.docs.apiary.io/) |
| [Delete User](actions/delete-user.md) | `DELETE /users/{idOrEmail}` | [docs](https://innform.docs.apiary.io/) |
| [Freeze User](actions/freeze-user.md) | `POST /users/{idOrEmail}/freeze` | [docs](https://innform.docs.apiary.io/) |
| [Get Group](actions/get-group.md) | `GET /groups/{id}` | [docs](https://innform.docs.apiary.io/) |
| [Get Property](actions/get-property.md) | `GET /properties/{id}` | [docs](https://innform.docs.apiary.io/) |
| [Get User](actions/get-user.md) | `GET /users/{idOrEmail}` | [docs](https://innform.docs.apiary.io/) |
| [Invite User](actions/invite-user.md) | `POST /users` | [docs](https://innform.docs.apiary.io/) |
| [List Assignments](actions/list-assignments.md) | `GET /assignments` | [docs](https://innform.docs.apiary.io/) |
| [List Courses](actions/list-courses.md) | `GET /courses` | [docs](https://innform.docs.apiary.io/) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://innform.docs.apiary.io/) |
| [List Learning Paths](actions/list-learning-paths.md) | `GET /learning_paths` | [docs](https://innform.docs.apiary.io/) |
| [List Properties](actions/list-properties.md) | `GET /properties` | [docs](https://innform.docs.apiary.io/) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://innform.docs.apiary.io/) |
| [Unfreeze User](actions/unfreeze-user.md) | `POST /users/{idOrEmail}/unfreeze` | [docs](https://innform.docs.apiary.io/) |
| [Update Group](actions/update-group.md) | `PUT /groups/{id}` | [docs](https://innform.docs.apiary.io/) |
| [Update Property](actions/update-property.md) | `PUT /properties/{id}` | [docs](https://innform.docs.apiary.io/) |
| [Update User](actions/update-user.md) | `PUT /users/{idOrEmail}` | [docs](https://innform.docs.apiary.io/) |
