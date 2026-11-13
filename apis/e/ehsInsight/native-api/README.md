# EHS Insight: Native API Reference

A consolidated summary of EHS Insight's API configuration and 19 documented operations.

- **API base URL:** `https://{companyName}.ehsinsight.com/api`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **Company Name:** `companyName` · optional

Send these headers with each API request:

```http
X-ApiKey: <apiKey>
```

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Entity](actions/add-entity.md) | `POST /v4/entity/:entityName/add` |  |
| [Create Business Entity](actions/create-business-entity.md) | `POST /v6/hierarchy/add` | [docs](https://qxobptest.ehsinsight.com/openapi/viewer?version=6&category=hierarchy#/Business%20Hierarchy/post_hierarchy_add) |
| [Create User Contact](actions/create-user-contact.md) | `POST /v6/entity/UserContact/add` | [docs](https://qxobptest.ehsinsight.com/site#/apidocumentation/v6/apidoc_entityapi_add) |
| [Delete User Contact](actions/delete-user-contact.md) | `GET /v6/entity/UserContact/delete/:rowUid` | [docs](https://qxobptest.ehsinsight.com/site#/apidocumentation/v6/apidoc_entityapi_delete) |
| [Get Attachment](actions/get-attachment.md) | `GET /v6/attachment/fetch/:rowUid` | [docs](https://qxobptest.ehsinsight.com/site#/apidocumentation/v6/apidoc_attachmentapi_attachment_fetch) |
| [Get Business Entity](actions/get-business-entity.md) | `GET /v6/hierarchy/fetch/:rowUid` | [docs](https://qxobptest.ehsinsight.com/openapi/viewer?version=6&category=hierarchy#/Business%20Hierarchy/get_hierarchy_fetch__RowUID_) |
| [Get SDS Community Attachment](actions/get-sds-community-attachment.md) | `GET /v6/sdscommunity/attachment/fetch/:rowUid` | [docs](https://qxobptest.ehsinsight.com/site#/apidocumentation/v6/apidoc_sdscommunityapi_attachment_fetch) |
| [Get Single Item](actions/get-single-item.md) | `GET /v4/entity/:entityName/fetch/:rowuid` |  |
| [Get User Contact](actions/get-user-contact.md) | `GET /v6/entity/UserContact/fetch/:rowUid` | [docs](https://qxobptest.ehsinsight.com/site#/apidocumentation/v6/apidoc_entityapi_fetch) |
| [List Business Entities](actions/list-business-entities.md) | `GET /v6/hierarchy/list` | [docs](https://qxobptest.ehsinsight.com/openapi/viewer?version=6&category=hierarchy#/Business%20Hierarchy/get_hierarchy_list) |
| [List Entities](actions/list-entities.md) | `GET /v6/entity/list?:customparams` | [docs](https://equixinctest.ehsinsight.com/openapi/viewer?version=6&category=entity) |
| [List Entity Items](actions/list-entity-items.md) | `GET /v6/entity/:entityName/list` | [docs](https://qxobptest.ehsinsight.com/site#/apidocumentation/v6/apidoc_entityapi_list) |
| [List Roles](actions/list-roles.md) | `GET /v6/role/list?:customparams` | [docs](https://equixinctest.ehsinsight.com/openapi/viewer?version=6&category=entity) |
| [List User Contacts with Parameters](actions/list-user-contacts-with-parameters.md) | `GET /v6/entity/UserContact/list` | [docs](https://qxobptest.ehsinsight.com/site#/apidocumentation/v6/apidoc_entityapi_list) |
| [Get Entity Schema](actions/new-action1.md) | `GET /v4/entity/:entityName/schema` |  |
| [Update Business Entity](actions/update-business-entity.md) | `POST /v6/hierarchy/update` | [docs](https://qxobptest.ehsinsight.com/openapi/viewer?version=6&category=hierarchy#/Business%20Hierarchy/post_hierarchy_update) |
| [Update Entity](actions/update-entity.md) | `POST /v4/entity/:entityName/update` |  |
| [Update User Contact](actions/update-user-contact.md) | `POST /v6/entity/UserContact/update` | [docs](https://qxobptest.ehsinsight.com/site#/apidocumentation/v6/apidoc_entityapi_update) |
| [Upload Attachment](actions/upload-attachment.md) | `POST /v6/attachment/add` | [docs](https://qxobptest.ehsinsight.com/site#/apidocumentation/v6/apidoc_attachmentapi_attachment_add) |
