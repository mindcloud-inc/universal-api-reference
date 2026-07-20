# Solace PubSub+ Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Solace PubSub+ expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-api-tokens?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Solace PubSub+ actions that support pagination

- [Get API Tokens](actions/get-api-tokens.md)
- [Get Application Domains](actions/get-application-domains.md)
- [Get Applications](actions/get-applications.md)
- [Get Broker Service Versions](actions/get-broker-service-versions.md)
- [Get Datacenters](actions/get-datacenters.md)
- [Get Default Broker Versions](actions/get-default-broker-versions.md)
- [Get Event Broker Services](actions/get-event-broker-services.md)
- [Get Events](actions/get-events.md)
- [Get Maintenance Activities](actions/get-maintenance-activities.md)
- [Get Maintenance Schedules](actions/get-maintenance-schedules.md)
- [Get Platform Environments](actions/get-platform-environments.md)
- [Get Resource Assignments](actions/get-resource-assignments.md)
- [Get Roles](actions/get-roles.md)
- [Get Service Classes](actions/get-service-classes.md)
- [Get Service Operations](actions/get-service-operations.md)
- [Get User Groups](actions/get-user-groups.md)
- [Get Users](actions/get-users.md)
