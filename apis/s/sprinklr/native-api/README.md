# Sprinklr: Native API Reference

A consolidated summary of Sprinklr's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://dev.sprinklr.com/api2-0
- **OpenAPI specification:** https://dev.sprinklr.com/portals/api/sites/spr-apigee-prod-apiprodportal/liveportal/apis/prod4/download_spec
- **API base URL:** `{apiBaseUrl}`

## Authentication

### OAuth 2.0

OAuth 2.0 authorization code flow for Sprinklr API 2.0 using the customer code-grant path.

### Credentials

- **API Base URL:** `apiBaseUrl` · required · Enter the tenant root URL used for OAuth and API calls, for example https://api3.sprinklr.com/prod4 or https://api3.sprinklr.com. Do not include /api/v2 in this value.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to {{credentials.apiBaseUrl}}/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to {{credentials.apiBaseUrl}}/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to {{credentials.apiBaseUrl}}/oauth/token.

[Official authentication documentation](https://dev.sprinklr.com/oauth-2-0-for-customers)

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Comment](actions/add-comment.md) | `POST api/v2/comment/{entityType}/{entityId}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fcomment%2F%7BentityType%7D%2F%7BentityId%7D/post) |
| [Create Case](actions/create-case.md) | `POST api/v2/case` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fcase/post) |
| [Create Custom Entity](actions/create-custom-entity.md) | `POST api/v2/custom-entity/entity` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fcustom-entity%2Fentity/post) |
| [Create Participant](actions/create-participant.md) | `POST api/v2/account/create-participant` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Faccount%2Fcreate-participant/post) |
| [Create Standard Entity](actions/create-standard-entity.md) | `POST api/v2/standard-entity/entity/{entityType}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fstandard-entity%2Fentity%2F%7BentityType%7D/post) |
| [Create Task](actions/create-task.md) | `POST api/v2/task` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Ftask/post) |
| [Delete Custom Entity](actions/delete-custom-entity.md) | `DELETE api/v2/custom-entity/entity/{entityType}/{entityId}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fcustom-entity%2Fentity%2F%7BentityType%7D%2F%7BentityId%7D/delete) |
| [Delete Standard Entity](actions/delete-standard-entity.md) | `DELETE api/v2/standard-entity/entity/{entityType}/{entityId}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fstandard-entity%2Fentity%2F%7BentityType%7D%2F%7BentityId%7D/delete) |
| [Delete Task](actions/delete-task.md) | `DELETE api/v2/task/{taskId}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Ftask%2F%7BtaskId%7D/delete) |
| [Get Account](actions/get-account.md) | `GET api/v2/account/{accountId}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Faccount%2F%7BaccountId%7D/get) |
| [Get Case](actions/get-case.md) | `GET api/v2/case/{caseId}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fcase%2F%7BcaseId%7D/get) |
| [Get Custom Entity](actions/get-custom-entity.md) | `GET api/v2/custom-entity/entity/{entityType}/{entityId}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fcustom-entity%2Fentity%2F%7BentityType%7D%2F%7BentityId%7D/get) |
| [Get Message](actions/get-message.md) | `GET api/v2/message` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fmessage/get) |
| [Get Participant](actions/get-participant.md) | `GET api/v2/account/get-participant/{participantId}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Faccount%2Fget-participant%2F%7BparticipantId%7D/get) |
| [Get Search Results Page](actions/get-search-results-page.md) | `GET api/v2/search/{entityType}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fsearch%2F%7BentityType%7D/get) |
| [Get Standard Entity](actions/get-standard-entity.md) | `GET api/v2/standard-entity/entity/{entityType}/{entityId}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fstandard-entity%2Fentity%2F%7BentityType%7D%2F%7BentityId%7D/get) |
| [Get Standard Entity By Primary Key](actions/get-standard-entity-by-primary-key.md) | `GET api/v2/standard-entity/entity/byPrimaryKey/{entityType}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fstandard-entity%2Fentity%2FbyPrimaryKey%2F%7BentityType%7D/get) |
| [Get Standard Entity Definition](actions/get-standard-entity-definition.md) | `GET api/v2/standard-entity/definition/{entityType}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fstandard-entity%2Fdefinition%2F%7BentityType%7D/get) |
| [Get Standard Entity Field](actions/get-standard-entity-field.md) | `GET api/v2/standard-entity/field/{entityType}/{fieldName}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fstandard-entity%2Ffield%2F%7BentityType%7D%2F%7BfieldName%7D/get) |
| [Get Task](actions/get-task.md) | `GET api/v2/task/{taskId}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Ftask%2F%7BtaskId%7D/get) |
| [Get Tasks](actions/get-tasks.md) | `GET api/v2/task` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Ftask/get) |
| [List Account Participants](actions/list-account-participants.md) | `GET api/v2/account/all-participants/{accountId}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Faccount%2Fall-participants%2F%7BaccountId%7D/get) |
| [List Case Messages](actions/list-case-messages.md) | `GET api/v2/case/associated-messages` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fcase%2Fassociated-messages/get) |
| [List Custom Entity Definitions](actions/list-custom-entity-definitions.md) | `GET api/v2/custom-entity/definitions` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fcustom-entity%2Fdefinitions/get) |
| [List Custom Entity Fields](actions/list-custom-entity-fields.md) | `GET api/v2/custom-entity/fields/{entityDefinitionId}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fcustom-entity%2Ffields%2F%7BentityDefinitionId%7D/get) |
| [List Standard Entity Fields](actions/list-standard-entity-fields.md) | `GET api/v2/standard-entity/fields/{entityType}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fstandard-entity%2Ffields%2F%7BentityType%7D/get) |
| [Patch Custom Entity](actions/patch-custom-entity.md) | `PATCH api/v2/custom-entity/entity/{entityType}/{entityId}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fcustom-entity%2Fentity%2F%7BentityType%7D%2F%7BentityId%7D/patch) |
| [Patch Standard Entity](actions/patch-standard-entity.md) | `PATCH api/v2/standard-entity/entity/{entityType}/{entityId}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fstandard-entity%2Fentity%2F%7BentityType%7D%2F%7BentityId%7D/patch) |
| [Perform Message Action](actions/perform-message-action.md) | `POST api/v2/message/action` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fmessage%2Faction/post) |
| [Search Entities](actions/search-entities.md) | `POST api/v2/search/{entityType}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fsearch%2F%7BentityType%7D/post) |
| [Search Profiles](actions/search-profiles.md) | `GET api/v2/profile/search` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fprofile%2Fsearch/get) |
| [Search Standard Entities By Primary Key Prefix](actions/search-standard-entities-by-primary-key-prefix.md) | `GET api/v2/standard-entity/entity/byPrimaryKeyPrefix/{entityType}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fstandard-entity%2Fentity%2FbyPrimaryKeyPrefix%2F%7BentityType%7D/get) |
| [Update Account Participant](actions/update-account-participant.md) | `POST api/v2/account/update-account-participant` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Faccount%2Fupdate-account-participant/post) |
| [Update Case](actions/update-case.md) | `PUT api/v2/case` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fcase/put) |
| [Update Custom Entity](actions/update-custom-entity.md) | `PUT api/v2/custom-entity/entity/{entityType}/{entityId}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fcustom-entity%2Fentity%2F%7BentityType%7D%2F%7BentityId%7D/put) |
| [Update Standard Entity](actions/update-standard-entity.md) | `PUT api/v2/standard-entity/entity/{entityType}/{entityId}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fstandard-entity%2Fentity%2F%7BentityType%7D%2F%7BentityId%7D/put) |
| [Update Task](actions/update-task.md) | `PUT api/v2/task/{taskId}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Ftask%2F%7BtaskId%7D/put) |
| [Upsert Custom Entity](actions/upsert-custom-entity.md) | `POST api/v2/custom-entity/entity/upsert` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fcustom-entity%2Fentity%2Fupsert/post) |
| [Upsert Standard Entity](actions/upsert-standard-entity.md) | `POST api/v2/standard-entity/entity/upsert/{entityType}/{entityId}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fstandard-entity%2Fentity%2Fupsert%2F%7BentityType%7D%2F%7BentityId%7D/post) |
| [Upsert Standard Entity By Primary Key](actions/upsert-standard-entity-by-primary-key.md) | `POST api/v2/standard-entity/entity/upsertByPrimaryKey/{entityType}` | [docs](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fstandard-entity%2Fentity%2FupsertByPrimaryKey%2F%7BentityType%7D/post) |
