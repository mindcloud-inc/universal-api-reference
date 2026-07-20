# Socie: Native API Reference

A consolidated summary of Socie's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://resources.socie.nl/docs/api/index.html
- **API base URL:** `https://api.socie.nl`

## Authentication

### API Key

Connect to Socie with a community API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://resources.socie.nl/docs/api/index.html)

## API conventions

Response data is read from `results`.

## Pagination

Use `limit` in the query string to set the page size. Use `skip` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Use `asc` for ascending order and `desc` for descending order. Multiple sort fields can be combined.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Additional Field](actions/add-additional-field.md) | `POST /api/v1/additional_fields` | [docs](https://resources.socie.nl/docs/api/resource_Additional_Fields.html#resource_Additional_Fields_addAdditionalField_context_additionalFieldInput_POST) |
| [Add Group](actions/add-group.md) | `POST /api/v1/groups` | [docs](https://resources.socie.nl/docs/api/resource_Groups.html#resource_Groups_addGroup_context_groupInput_POST) |
| [Add Group Membership](actions/add-group-membership.md) | `POST /api/v1/groups/:groupIdentifier/memberships` | [docs](https://resources.socie.nl/docs/api/resource_Groups.html#resource_Groups_addGroupMembership_context_groupMembershipInput_groupIdentifier_groupsKey_POST) |
| [Add Group Memberships in Bulk](actions/add-group-memberships-in-bulk.md) | `POST /api/v1/groups/:groupIdentifier/memberships/_bulk` | [docs](https://resources.socie.nl/docs/api/resource_Groups.html#resource_Groups_addGroupMemberships_context_groupMembershipsInput_groupIdentifier_groupsKey_POST) |
| [Add Member](actions/add-member.md) | `POST /api/v1/members` | [docs](https://resources.socie.nl/docs/api/resource_Members.html#resource_Members_addMember_context_memberInput_POST) |
| [Add Members in Bulk](actions/add-members-in-bulk.md) | `POST /api/v1/members/_bulk` | [docs](https://resources.socie.nl/docs/api/resource_Members.html#resource_Members_addMembers_context_membersInput_POST) |
| [Delete Additional Field](actions/delete-additional-field.md) | `DELETE /api/v1/additional_fields/:identifier` | [docs](https://resources.socie.nl/docs/api/resource_Additional_Fields.html#resource_Additional_Fields_deleteAdditionalField_context_identifier_DELETE) |
| [Delete Group](actions/delete-group.md) | `DELETE /api/v1/groups/:identifier` | [docs](https://resources.socie.nl/docs/api/resource_Groups.html#resource_Groups_deleteGroup_context_identifier_key_DELETE) |
| [Delete Group Membership](actions/delete-group-membership.md) | `DELETE /api/v1/groups/:groupIdentifier/memberships/:identifier` | [docs](https://resources.socie.nl/docs/api/resource_Groups.html#resource_Groups_deleteGroupMembership_context_groupIdentifier_groupsKey_identifier_key_DELETE) |
| [Delete Member](actions/delete-member.md) | `DELETE /api/v1/members/:identifier` | [docs](https://resources.socie.nl/docs/api/resource_Members.html#resource_Members_deleteMember_context_identifier_key_DELETE) |
| [Get Additional Field](actions/get-additional-field.md) | `GET /api/v1/additional_fields/:identifier` | [docs](https://resources.socie.nl/docs/api/resource_Additional_Fields.html#resource_Additional_Fields_getAdditionalField_context_identifier_GET) |
| [Get Group](actions/get-group.md) | `GET /api/v1/groups/:identifier` | [docs](https://resources.socie.nl/docs/api/resource_Groups.html#resource_Groups_getGroup_context_identifier_key_GET) |
| [Get Group Membership](actions/get-group-membership.md) | `GET /api/v1/groups/:groupIdentifier/memberships/:identifier` | [docs](https://resources.socie.nl/docs/api/resource_Groups.html#resource_Groups_getGroupMembership_context_groupIdentifier_groupsKey_identifier_key_GET) |
| [Get Member](actions/get-member.md) | `GET /api/v1/members/:identifier` | [docs](https://resources.socie.nl/docs/api/resource_Members.html#resource_Members_getMember_context_identifier_key_GET) |
| [List Additional Fields](actions/list-additional-fields.md) | `GET /api/v1/additional_fields` | [docs](https://resources.socie.nl/docs/api/resource_Additional_Fields.html#resource_Additional_Fields_getAdditionalFields_context_sort_skip_limit_GET) |
| [List Group Memberships](actions/list-group-memberships.md) | `GET /api/v1/groups/:groupIdentifier/memberships` | [docs](https://resources.socie.nl/docs/api/resource_Groups.html#resource_Groups_getGroupMemberships_context_groupIdentifier_groupsKey_sort_skip_limit_GET) |
| [List Groups](actions/list-groups.md) | `GET /api/v1/groups` | [docs](https://resources.socie.nl/docs/api/resource_Groups.html#resource_Groups_getGroups_context_sort_skip_limit_GET) |
| [List Members](actions/list-members.md) | `GET /api/v1/members` | [docs](https://resources.socie.nl/docs/api/resource_Members.html#resource_Members_getMembers_context_sort_skip_limit_GET) |
| [Send or Schedule Notification](actions/send-or-schedule-notification.md) | `POST /api/v1/notifications` | [docs](https://resources.socie.nl/docs/api/resource_Notifications.html#resource_Notifications_sendNotification_context_input_POST) |
| [Trigger Importing Groups](actions/trigger-importing-groups.md) | `POST /api/v1/triggers/groups/import` | [docs](https://resources.socie.nl/docs/api/resource_Triggers.html#resource_Triggers_triggerGroupsImport_context_api_key_POST) |
| [Trigger Importing Members](actions/trigger-importing-members.md) | `POST /api/v1/triggers/members/import` | [docs](https://resources.socie.nl/docs/api/resource_Triggers.html#resource_Triggers_triggerMembersImport_context_api_key_POST) |
| [Update Additional Field](actions/update-additional-field.md) | `PATCH /api/v1/additional_fields/:identifier` | [docs](https://resources.socie.nl/docs/api/resource_Additional_Fields.html#resource_Additional_Fields_updateAdditionalField_context_identifier_additionalFieldInput_PATCH) |
| [Update Group](actions/update-group.md) | `PATCH /api/v1/groups/:identifier` | [docs](https://resources.socie.nl/docs/api/resource_Groups.html#resource_Groups_updateGroup_context_identifier_groupInput_key_PATCH) |
| [Update Group Membership](actions/update-group-membership.md) | `PATCH /api/v1/groups/:groupIdentifier/memberships/:identifier` | [docs](https://resources.socie.nl/docs/api/resource_Groups.html#resource_Groups_updateGroupMembership_context_groupIdentifier_groupsKey_identifier_key_patchInput_PATCH) |
| [Update Group Memberships Order](actions/update-group-memberships-order.md) | `PATCH /api/v1/groups/:groupIdentifier/memberships/order` | [docs](https://resources.socie.nl/docs/api/resource_Groups.html#resource_Groups_updateGroupMembershipsOrder_context_groupIdentifier_groupsKey_orderInput_PATCH) |
| [Update Member](actions/update-member.md) | `PATCH /api/v1/members/:identifier` | [docs](https://resources.socie.nl/docs/api/resource_Members.html#resource_Members_updateMember_context_identifier_memberInput_key_PATCH) |
