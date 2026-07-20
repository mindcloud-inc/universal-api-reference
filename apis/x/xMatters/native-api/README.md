# xMatters: Native API Reference

A consolidated summary of xMatters's API configuration and 164 documented operations, with links to official documentation.

- **Official docs:** https://help.xmatters.com/xmapi/index.html
- **API base URL:** `https://mindcloud.xmatters.com/api/xm/1`

## Authentication

### Basic Authentication

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://help.xmatters.com/xmapi/index.html#http-basic-authentication)

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `offset` in the query string as the record offset.

## Sorting

Set the sort field with `sortBy` in the query string. Set the direction separately with `sortOrder`. Use `ASCENDING` for ascending order and `DESCENDING` for descending order. Only one sort field is accepted.

## Endpoints (164 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add a comment to an event](actions/add-a-comment-to-an-event.md) | `POST events/{eventId}/annotations` | [docs](https://help.xmatters.com/xmapi/index.html#add-a-comment-to-an-event) |
| [Add a member to a shift](actions/add-a-member-to-a-shift.md) | `POST groups/{groupId}/shifts/{shiftId}/members` | [docs](https://help.xmatters.com/xmapi/index.html#add-a-member-to-a-shift) |
| [Add a member to the group](actions/add-a-member-to-the-group.md) | `POST groups/{groupId}/members` | [docs](https://help.xmatters.com/xmapi/index.html#add-a-member-to-the-group) |
| [Add a timeline note](actions/add-a-timeline-note.md) | `POST incidents/{incidentId}/timeline-entries` | [docs](https://help.xmatters.com/xmapi/index.html#add-a-timeline-note) |
| [Add subscribers](actions/add-subscribers.md) | `PUT subscriptions/{subscriptionId}/subscribers` | [docs](https://help.xmatters.com/xmapi/index.html#add-subscribers) |
| [Change the status of an event](actions/change-the-status-of-an-event.md) | `POST events` | [docs](https://help.xmatters.com/xmapi/index.html#change-the-status-of-an-event) |
| [Create a change record](actions/create-a-change-record.md) | `POST changes` | [docs](https://help.xmatters.com/xmapi/index.html#create-a-change-record) |
| [Create a communication plan](actions/create-a-communication-plan.md) | `POST plans` | [docs](https://help.xmatters.com/xmapi/index.html#create-a-communication-plan) |
| [Create a device](actions/create-a-device.md) | `POST devices` | [docs](https://help.xmatters.com/xmapi/index.html#create-a-device) |
| [Create a device name](actions/create-a-device-name.md) | `POST deviceName` | [docs](https://help.xmatters.com/xmapi/index.html#create-a-device-name) |
| [Create a form section](actions/create-a-form-section.md) | `POST forms/{formId}/sections` | [docs](https://help.xmatters.com/xmapi/index.html#create-a-form-section) |
| [Create a group](actions/create-a-group.md) | `POST groups` | [docs](https://help.xmatters.com/xmapi/index.html#create-a-group) |
| [Create a person](actions/create-a-person.md) | `POST people` | [docs](https://help.xmatters.com/xmapi/index.html#create-a-person) |
| [Create a plan constant](actions/create-a-plan-constant.md) | `POST plans/{planId}/constants` | [docs](https://help.xmatters.com/xmapi/index.html#create-a-plan-constant) |
| [Create a plan form](actions/create-a-plan-form.md) | `POST plans/{planId}/forms` | [docs](https://help.xmatters.com/xmapi/index.html#create-a-plan-form) |
| [Create a scenario](actions/create-a-scenario.md) | `POST forms/{formId}/scenarios` | [docs](https://help.xmatters.com/xmapi/index.html#create-a-scenario) |
| [Create a scheduled message](actions/create-a-scheduled-message.md) | `POST scheduled-messages` | [docs](https://help.xmatters.com/xmapi/index.html#create-a-scheduled-message) |
| [Create a service](actions/create-a-service.md) | `POST services` | [docs](https://help.xmatters.com/xmapi/index.html#create-a-service) |
| [Create a service dependency](actions/create-a-service-dependency.md) | `POST service-dependencies` | [docs](https://help.xmatters.com/xmapi/index.html#create-a-service-dependency) |
| [Create a shared library](actions/create-a-shared-library.md) | `POST shared-libraries` | [docs](https://help.xmatters.com/xmapi/index.html#create-a-shared-library) |
| [Create a shift](actions/create-a-shift.md) | `POST groups/{groupId}/shifts` | [docs](https://help.xmatters.com/xmapi/index.html#create-a-shift) |
| [Create a site](actions/create-a-site.md) | `POST sites` | [docs](https://help.xmatters.com/xmapi/index.html#create-a-site) |
| [Create a subscription](actions/create-a-subscription.md) | `POST subscriptions` | [docs](https://help.xmatters.com/xmapi/index.html#create-a-subscription) |
| [Create a subscription form](actions/create-a-subscription-form.md) | `POST plans/{planId}/subscription-forms` | [docs](https://help.xmatters.com/xmapi/index.html#create-a-subscription-form) |
| [Create a temporary absence](actions/create-a-temporary-absence.md) | `POST temporary-absences` | [docs](https://help.xmatters.com/xmapi/index.html#create-a-temporary-absence) |
| [Create an external conference bridge](actions/create-an-external-conference-bridge.md) | `POST conference-bridges` | [docs](https://help.xmatters.com/xmapi/index.html#create-an-external-conference-bridge) |
| [Create an incident](actions/create-an-incident.md) | `POST incidents` | [docs](https://help.xmatters.com/xmapi/index.html#create-an-incident) |
| [Create an integration](actions/create-an-integration.md) | `POST plans/{planId}/integrations` | [docs](https://help.xmatters.com/xmapi/index.html#create-an-integration) |
| [Create form message templates](actions/create-form-message-templates.md) | `POST forms/{formId}/message-templates` | [docs](https://help.xmatters.com/xmapi/index.html#create-form-message-templates) |
| [Create form response options](actions/create-form-response-options.md) | `POST forms/{formId}/response-options` | [docs](https://help.xmatters.com/xmapi/index.html#create-form-response-options) |
| [Create plan endpoint](actions/create-plan-endpoint.md) | `POST plans/{planId}/endpoints` | [docs](https://help.xmatters.com/xmapi/index.html#create-plan-endpoint) |
| [Create plan properties](actions/create-plan-properties.md) | `POST plans/{planId}/property-definitions` | [docs](https://help.xmatters.com/xmapi/index.html#create-plan-properties) |
| [Delete a conference bridge](actions/delete-a-conference-bridge.md) | `DELETE conference-bridges/{conferenceBridgeId}` | [docs](https://help.xmatters.com/xmapi/index.html#delete-a-conference-bridge) |
| [Delete a device](actions/delete-a-device.md) | `DELETE devices/{deviceId}` | [docs](https://help.xmatters.com/xmapi/index.html#delete-a-device) |
| [Delete a device name](actions/delete-a-device-name.md) | `DELETE device-names/{deviceNameId}` | [docs](https://help.xmatters.com/xmapi/index.html#delete-a-device-name) |
| [Delete a group](actions/delete-a-group.md) | `DELETE groups/{groupId}` | [docs](https://help.xmatters.com/xmapi/index.html#delete-a-group) |
| [Delete a person](actions/delete-a-person.md) | `DELETE people/{personId}` | [docs](https://help.xmatters.com/xmapi/index.html#delete-a-person) |
| [Delete a plan](actions/delete-a-plan.md) | `DELETE plans/{planId}` | [docs](https://help.xmatters.com/xmapi/index.html#delete-a-plan) |
| [Delete a plan constant](actions/delete-a-plan-constant.md) | `DELETE plans/{planId}/constants/{constantId}` | [docs](https://help.xmatters.com/xmapi/index.html#delete-a-plan-constant) |
| [Delete a plan endpoint](actions/delete-a-plan-endpoint.md) | `DELETE plans/{planId}/endpoints/{endpointId}` | [docs](https://help.xmatters.com/xmapi/index.html#delete-a-plan-endpoint) |
| [Delete a scheduled message](actions/delete-a-scheduled-message.md) | `DELETE scheduled-messages/{scheduledMessageId}` | [docs](https://help.xmatters.com/xmapi/index.html#delete-a-scheduled-message) |
| [Delete a service](actions/delete-a-service.md) | `DELETE services/{serviceId}` | [docs](https://help.xmatters.com/xmapi/index.html#delete-a-service) |
| [Delete a service dependency](actions/delete-a-service-dependency.md) | `DELETE service-dependencies/{serviceDependencyId}` | [docs](https://help.xmatters.com/xmapi/index.html#delete-a-service-dependency) |
| [Delete a shared library](actions/delete-a-shared-library.md) | `DELETE shared-libraries/{sharedLibraryId}` | [docs](https://help.xmatters.com/xmapi/index.html#delete-a-shared-library) |
| [Delete a shift](actions/delete-a-shift.md) | `DELETE groups/{groupId}/shifts/{shiftId}` | [docs](https://help.xmatters.com/xmapi/index.html#delete-a-shift) |
| [Delete a site](actions/delete-a-site.md) | `DELETE sites/{siteId}` | [docs](https://help.xmatters.com/xmapi/index.html#delete-a-site) |
| [Delete a subscription](actions/delete-a-subscription.md) | `DELETE subscriptions/{subscriptionId}` | [docs](https://help.xmatters.com/xmapi/index.html#delete-a-subscription) |
| [Delete a temporary absence](actions/delete-a-temporary-absence.md) | `DELETE temporary-absences/{temporaryAbsenceId}` | [docs](https://help.xmatters.com/xmapi/index.html#delete-a-temporary-absence) |
| [Delete an integration](actions/delete-an-integration.md) | `DELETE plans/{planId}/integrations/{integrationId}` | [docs](https://help.xmatters.com/xmapi/index.html#delete-an-integration) |
| [Get a change](actions/get-a-change.md) | `GET changes/{changeId}` | [docs](https://help.xmatters.com/xmapi/index.html#get-a-change) |
| [Get a communication plan](actions/get-a-communication-plan.md) | `GET plans/{planId}` | [docs](https://help.xmatters.com/xmapi/index.html#get-a-communication-plan) |
| [Get a conference bridge](actions/get-a-conference-bridge.md) | `GET conference-bridges/{conferenceBridgeId}` | [docs](https://help.xmatters.com/xmapi/index.html#get-a-conference-bridge) |
| [Get a device](actions/get-a-device.md) | `GET devices/{deviceId}` | [docs](https://help.xmatters.com/xmapi/index.html#get-a-device) |
| [Get a form in a plan](actions/get-a-form-in-a-plan.md) | `GET plans/{planId}/forms/{formId}` | [docs](https://help.xmatters.com/xmapi/index.html#get-a-form-in-a-plan) |
| [Get a group](actions/get-a-group.md) | `GET groups/{groupId}` | [docs](https://help.xmatters.com/xmapi/index.html#get-a-group) |
| [Get a group's recipients](actions/get-a-group-s-recipients.md) | `GET groups/{groupId}/recipients` | [docs](https://help.xmatters.com/xmapi/index.html#get-a-group-39-s-recipients) |
| [Get a group's supervisors](actions/get-a-group-s-supervisors.md) | `GET groups/{groupId}/supervisors` | [docs](https://help.xmatters.com/xmapi/index.html#get-a-group-39-s-supervisors) |
| [Get a person (by id)](actions/get-a-person-by-id.md) | `GET people/{personId}` | [docs](https://help.xmatters.com/xmapi/index.html#get-a-person-by-id) |
| [Get a person's devices](actions/get-a-person-s-devices.md) | `GET people/{personId}/devices` | [docs](https://help.xmatters.com/xmapi/index.html#get-a-person-39-s-devices) |
| [Get a person's groups](actions/get-a-person-s-groups.md) | `GET people/{personId}/group-memberships` | [docs](https://help.xmatters.com/xmapi/index.html#get-a-person-39-s-groups) |
| [Get a person's supervisors](actions/get-a-person-s-supervisors.md) | `GET people/{personId}/supervisors` | [docs](https://help.xmatters.com/xmapi/index.html#get-a-person-39-s-supervisors) |
| [Get a scenario](actions/get-a-scenario.md) | `GET scenarios/{scenarioId}` | [docs](https://help.xmatters.com/xmapi/index.html#get-a-scenario) |
| [Get a scenario attachment](actions/get-a-scenario-attachment.md) | `GET scenarios/{scenarioId}/attachments/{attachmentId}` | [docs](https://help.xmatters.com/xmapi/index.html#get-a-scenario-attachment) |
| [Get a scheduled message](actions/get-a-scheduled-message.md) | `GET scheduled-messages/{scheduledMessageId}` | [docs](https://help.xmatters.com/xmapi/index.html#get-a-scheduled-message) |
| [Get a scheduled message attachment](actions/get-a-scheduled-message-attachment.md) | `GET scheduled-messages/{scheduledMessageId}/attachments/{attachmentId}` | [docs](https://help.xmatters.com/xmapi/index.html#get-a-scheduled-message-attachment) |
| [Get a service](actions/get-a-service.md) | `GET services/{serviceId}` | [docs](https://help.xmatters.com/xmapi/index.html#get-a-service) |
| [Get a shared library](actions/get-a-shared-library.md) | `GET shared-libraries/{sharedLibraryId}` | [docs](https://help.xmatters.com/xmapi/index.html#get-a-shared-library) |
| [Get a shift](actions/get-a-shift.md) | `GET groups/{groupId}/shifts/{shiftId}` | [docs](https://help.xmatters.com/xmapi/index.html#get-a-shift) |
| [Get a signal](actions/get-a-signal.md) | `GET signals/{signalId}` | [docs](https://help.xmatters.com/xmapi/index.html#get-a-signal) |
| [Get a site](actions/get-a-site.md) | `GET sites/{siteId}` | [docs](https://help.xmatters.com/xmapi/index.html#get-a-site) |
| [Get a subscription](actions/get-a-subscription.md) | `GET subscriptions/{subscriptionId}` | [docs](https://help.xmatters.com/xmapi/index.html#get-a-subscription) |
| [Get a subscription form](actions/get-a-subscription-form.md) | `GET subscription-forms/{subscriptionFormId}` | [docs](https://help.xmatters.com/xmapi/index.html#get-a-subscription-form) |
| [Get an event](actions/get-an-event.md) | `GET events/{eventId}` | [docs](https://help.xmatters.com/xmapi/index.html#get-an-event) |
| [Get an event annotation](actions/get-an-event-annotation.md) | `GET events/{eventId}/annotations/{annotationId}` | [docs](https://help.xmatters.com/xmapi/index.html#get-an-event-annotation) |
| [Get an event attachment](actions/get-an-event-attachment.md) | `GET events/{eventId}/attachments/{attachmentId}` | [docs](https://help.xmatters.com/xmapi/index.html#get-an-event-attachment) |
| [Get an import job](actions/get-an-import-job.md) | `GET imports/{importId}` | [docs](https://help.xmatters.com/xmapi/index.html#get-an-import-job) |
| [Get an incident](actions/get-an-incident.md) | `GET incidents/{incidentId}` | [docs](https://help.xmatters.com/xmapi/index.html#get-an-incident) |
| [Get an integration](actions/get-an-integration.md) | `GET plans/{planId}/integrations/{integrationId}` | [docs](https://help.xmatters.com/xmapi/index.html#get-an-integration) |
| [Get changes](actions/get-changes.md) | `GET changes` | [docs](https://help.xmatters.com/xmapi/index.html#get-changes) |
| [Get communication plans](actions/get-communication-plans.md) | `GET plans` | [docs](https://help.xmatters.com/xmapi/index.html#get-communication-plans) |
| [Get conference bridges](actions/get-conference-bridges.md) | `GET conference-bridges` | [docs](https://help.xmatters.com/xmapi/index.html#get-conference-bridges) |
| [Get deleted shift occurrences](actions/get-deleted-shift-occurrences.md) | `GET groups/{groupId}/shifts/{shiftId}/exclusions` | [docs](https://help.xmatters.com/xmapi/index.html#get-deleted-shift-occurrences) |
| [Get device names](actions/get-device-names.md) | `GET device-names` | [docs](https://help.xmatters.com/xmapi/index.html#get-device-names) |
| [Get device types](actions/get-device-types.md) | `GET device-types` | [docs](https://help.xmatters.com/xmapi/index.html#get-device-types) |
| [Get devices](actions/get-devices.md) | `GET devices` | [docs](https://help.xmatters.com/xmapi/index.html#get-devices) |
| [Get event annotations](actions/get-event-annotations.md) | `GET events/{eventId}/annotations` | [docs](https://help.xmatters.com/xmapi/index.html#get-event-annotations) |
| [Get event audit information](actions/get-event-audit-information.md) | `GET audits` | [docs](https://help.xmatters.com/xmapi/index.html#get-event-audit-information) |
| [Get events](actions/get-events.md) | `GET events` | [docs](https://help.xmatters.com/xmapi/index.html#get-events) |
| [Get form response options](actions/get-form-response-options.md) | `GET plans/{planId}/forms/{formId}/response-options` | [docs](https://help.xmatters.com/xmapi/index.html#get-form-response-options) |
| [Get form sections](actions/get-form-sections.md) | `GET forms/{formId}/sections` | [docs](https://help.xmatters.com/xmapi/index.html#get-form-sections) |
| [Get forms](actions/get-forms.md) | `GET forms` | [docs](https://help.xmatters.com/xmapi/index.html#get-forms) |
| [Get forms in a plan](actions/get-forms-in-a-plan.md) | `GET plans/{planId}/forms` | [docs](https://help.xmatters.com/xmapi/index.html#get-forms-in-a-plan) |
| [Get group license quotas](actions/get-group-license-quotas.md) | `GET groups/license-quotas` | [docs](https://help.xmatters.com/xmapi/index.html#get-group-license-quotas) |
| [Get group members](actions/get-group-members.md) | `GET groups/{groupId}/members` | [docs](https://help.xmatters.com/xmapi/index.html#get-group-members) |
| [Get groups](actions/get-groups.md) | `GET groups` | [docs](https://help.xmatters.com/xmapi/index.html#get-groups) |
| [Get import job messages](actions/get-import-job-messages.md) | `GET imports/{importId}/import-messages` | [docs](https://help.xmatters.com/xmapi/index.html#get-import-job-messages) |
| [Get import jobs](actions/get-import-jobs.md) | `GET imports` | [docs](https://help.xmatters.com/xmapi/index.html#get-import-jobs) |
| [Get incidents](actions/get-incidents.md) | `GET incidents` | [docs](https://help.xmatters.com/xmapi/index.html#get-incidents) |
| [Get integration logs](actions/get-integration-logs.md) | `GET integrations/{integrationId}/logs` | [docs](https://help.xmatters.com/xmapi/index.html#get-integration-logs) |
| [Get integrations](actions/get-integrations.md) | `GET plans/{planId}/integrations` | [docs](https://help.xmatters.com/xmapi/index.html#get-integrations) |
| [Get members in a shift](actions/get-members-in-a-shift.md) | `GET groups/{groupId}/shifts/{shiftId}/members` | [docs](https://help.xmatters.com/xmapi/index.html#get-members-in-a-shift) |
| [Get on-call summary](actions/get-on-call-summary.md) | `GET on-call-summary` | [docs](https://help.xmatters.com/xmapi/index.html#get-on-call-summary) |
| [Get People](actions/get-people.md) | `GET people` | [docs](https://help.xmatters.com/xmapi/index.html#get-people) |
| [Get plan constants](actions/get-plan-constants.md) | `GET plans/{planId}/constants` | [docs](https://help.xmatters.com/xmapi/index.html#get-plan-constants) |
| [Get plan endpoints](actions/get-plan-endpoints.md) | `GET plans/{planId}/endpoints` | [docs](https://help.xmatters.com/xmapi/index.html#get-plan-endpoints) |
| [Get plan properties](actions/get-plan-properties.md) | `GET plans/{planId}/property-definitions` | [docs](https://help.xmatters.com/xmapi/index.html#get-plan-properties) |
| [Get roles](actions/get-roles.md) | `GET roles` | [docs](https://help.xmatters.com/xmapi/index.html#get-roles) |
| [Get scenario sender permissions](actions/get-scenario-sender-permissions.md) | `GET scenarios/{scenarioId}/sender-permissions` | [docs](https://help.xmatters.com/xmapi/index.html#get-scenario-sender-permissions) |
| [Get scenarios](actions/get-scenarios.md) | `GET scenarios` | [docs](https://help.xmatters.com/xmapi/index.html#get-scenarios) |
| [Get scenarios in a form](actions/get-scenarios-in-a-form.md) | `GET plans/{planId}/forms/{formId}/scenarios` | [docs](https://help.xmatters.com/xmapi/index.html#get-scenarios-in-a-form) |
| [Get scheduled messages](actions/get-scheduled-messages.md) | `GET scheduled-messages` | [docs](https://help.xmatters.com/xmapi/index.html#get-scheduled-messages) |
| [Get service dependencies](actions/get-service-dependencies.md) | `GET service-dependencies` | [docs](https://help.xmatters.com/xmapi/index.html#get-service-dependencies) |
| [Get services](actions/get-services.md) | `GET services` | [docs](https://help.xmatters.com/xmapi/index.html#get-services) |
| [Get shared libraries](actions/get-shared-libraries.md) | `GET plans/{planId}/shared-libraries` | [docs](https://help.xmatters.com/xmapi/index.html#get-shared-libraries) |
| [Get shift occurrences](actions/get-shift-occurrences.md) | `GET groups/{groupId}/occurrences` | [docs](https://help.xmatters.com/xmapi/index.html#get-shift-occurrences) |
| [Get shifts](actions/get-shifts.md) | `GET groups/{groupId}/shifts` | [docs](https://help.xmatters.com/xmapi/index.html#get-shifts) |
| [Get signals](actions/get-signals.md) | `GET groups/{groupId}/signals` | [docs](https://help.xmatters.com/xmapi/index.html#get-signals) |
| [Get sites](actions/get-sites.md) | `GET sites` | [docs](https://help.xmatters.com/xmapi/index.html#get-sites) |
| [Get subscribers](actions/get-subscribers.md) | `GET subscriptions/{subscriptionId}/subscribers` | [docs](https://help.xmatters.com/xmapi/index.html#get-subscribers) |
| [Get subscription forms](actions/get-subscription-forms.md) | `GET subscription-forms` | [docs](https://help.xmatters.com/xmapi/index.html#get-subscription-forms) |
| [Get subscription forms in a plan](actions/get-subscription-forms-in-a-plan.md) | `GET plans/{planId}/subscription-forms` | [docs](https://help.xmatters.com/xmapi/index.html#get-subscription-forms-in-a-plan) |
| [Get subscription share permissions](actions/get-subscription-share-permissions.md) | `GET subscriptions/{subscriptionId}/share-permissions` | [docs](https://help.xmatters.com/xmapi/index.html#get-subscription-share-permissions) |
| [Get subscriptions](actions/get-subscriptions.md) | `GET subscriptions` | [docs](https://help.xmatters.com/xmapi/index.html#get-subscriptions) |
| [Get suppressed events](actions/get-suppressed-events.md) | `GET event-suppressions` | [docs](https://help.xmatters.com/xmapi/index.html#get-suppressed-events) |
| [Get temporary absences](actions/get-temporary-absences.md) | `GET temporary-absences` | [docs](https://help.xmatters.com/xmapi/index.html#get-temporary-absences) |
| [Get user delivery data](actions/get-user-delivery-data.md) | `GET events/{eventId}/user-deliveries` | [docs](https://help.xmatters.com/xmapi/index.html#get-user-delivery-data) |
| [Get user license quotas](actions/get-user-license-quotas.md) | `GET people/license-quotas` | [docs](https://help.xmatters.com/xmapi/index.html#get-user-license-quotas) |
| [Get who is on call](actions/get-who-is-on-call.md) | `GET on-call` | [docs](https://help.xmatters.com/xmapi/index.html#get-who-is-on-call) |
| [Modify a conference bridge](actions/modify-a-conference-bridge.md) | `POST conference-bridges` | [docs](https://help.xmatters.com/xmapi/index.html#modify-a-conference-bridge) |
| [Modify a device](actions/modify-a-device.md) | `POST devices` | [docs](https://help.xmatters.com/xmapi/index.html#modify-a-device) |
| [Modify a device name](actions/modify-a-device-name.md) | `POST device-names` | [docs](https://help.xmatters.com/xmapi/index.html#modify-a-device-name) |
| [Modify a form message template](actions/modify-a-form-message-template.md) | `POST forms/{formId}/message-templates` | [docs](https://help.xmatters.com/xmapi/index.html#modify-a-form-message-template) |
| [Modify a form response option](actions/modify-a-form-response-option.md) | `POST forms/{formId}/response-options` | [docs](https://help.xmatters.com/xmapi/index.html#modify-a-form-response-option) |
| [Modify a form section](actions/modify-a-form-section.md) | `POST forms/{formId}/sections` | [docs](https://help.xmatters.com/xmapi/index.html#modify-a-form-section) |
| [Modify a group](actions/modify-a-group.md) | `POST groups` | [docs](https://help.xmatters.com/xmapi/index.html#modify-a-group) |
| [Modify a person](actions/modify-a-person.md) | `POST people` | [docs](https://help.xmatters.com/xmapi/index.html#modify-a-person) |
| [Modify a plan constant](actions/modify-a-plan-constant.md) | `POST plans/{planId}/constants` | [docs](https://help.xmatters.com/xmapi/index.html#modify-a-plan-constant) |
| [Modify a plan endpoint](actions/modify-a-plan-endpoint.md) | `POST plans/{planId}/endpoints` | [docs](https://help.xmatters.com/xmapi/index.html#modify-a-plan-endpoint) |
| [Modify a plan form](actions/modify-a-plan-form.md) | `POST plans/{planId}/forms` | [docs](https://help.xmatters.com/xmapi/index.html#modify-a-plan-form) |
| [Modify a scenario](actions/modify-a-scenario.md) | `POST forms/{formId}/scenarios` | [docs](https://help.xmatters.com/xmapi/index.html#modify-a-scenario) |
| [Modify a scheduled message](actions/modify-a-scheduled-message.md) | `POST scheduled-messages` | [docs](https://help.xmatters.com/xmapi/index.html#modify-a-scheduled-message) |
| [Modify a service](actions/modify-a-service.md) | `POST services` | [docs](https://help.xmatters.com/xmapi/index.html#modify-a-service) |
| [Modify a service dependency](actions/modify-a-service-dependency.md) | `POST service-dependencies` | [docs](https://help.xmatters.com/xmapi/index.html#modify-a-service-dependency) |
| [Modify a shared library](actions/modify-a-shared-library.md) | `POST shared-libraries` | [docs](https://help.xmatters.com/xmapi/index.html#modify-a-shared-library) |
| [Modify a site](actions/modify-a-site.md) | `POST sites` | [docs](https://help.xmatters.com/xmapi/index.html#modify-a-site) |
| [Modify a subscription](actions/modify-a-subscription.md) | `POST subscriptions` | [docs](https://help.xmatters.com/xmapi/index.html#modify-a-subscription) |
| [Modify a subscription form](actions/modify-a-subscription-form.md) | `POST plans/{planId}/subscription-forms` | [docs](https://help.xmatters.com/xmapi/index.html#modify-a-subscription-form) |
| [Modify an incident](actions/modify-an-incident.md) | `POST incidents` | [docs](https://help.xmatters.com/xmapi/index.html#modify-an-incident) |
| [Modify an Integration](actions/modify-an-integration.md) | `POST plans/{planId}/integrations` | [docs](https://help.xmatters.com/xmapi/index.html#modify-an-integration) |
| [Modify communication plan](actions/modify-communication-plan.md) | `POST plans` | [docs](https://help.xmatters.com/xmapi/index.html#modify-communication-plan) |
| [Modify plan properties](actions/modify-plan-properties.md) | `POST plans/{planId}/property-definitions` | [docs](https://help.xmatters.com/xmapi/index.html#modify-plan-properties) |
| [Remove a member from the group](actions/remove-a-member-from-the-group.md) | `DELETE groups/{groupId}/members/{memberId}` | [docs](https://help.xmatters.com/xmapi/index.html#remove-a-member-from-the-group) |
| [Restore deleted shift occurrences](actions/restore-deleted-shift-occurrences.md) | `POST groups/{groupId}/shifts/{shiftId}/occurrences` | [docs](https://help.xmatters.com/xmapi/index.html#restore-deleted-shift-occurrences) |
| [Set scenario sender permissions](actions/set-scenario-sender-permissions.md) | `PUT scenarios/{scenarioId}/sender-permissions` | [docs](https://help.xmatters.com/xmapi/index.html#set-scenario-sender-permissions) |
| [Set subscription share permissions](actions/set-subscription-share-permissions.md) | `PUT subscriptions/{subscriptionId}/share-permissions` | [docs](https://help.xmatters.com/xmapi/index.html#set-subscription-share-permissions) |
| [Trigger an incident](actions/trigger-an-incident.md) | `POST forms/{formId}/triggers` | [docs](https://help.xmatters.com/xmapi/index.html#trigger-an-incident) |
| [Unsubscribe a user](actions/unsubscribe-a-user.md) | `DELETE subscriptions/{subscriptionId}/subscribers/{subscriberId}` | [docs](https://help.xmatters.com/xmapi/index.html#unsubscribe-a-user) |
| [Update a shift](actions/update-a-shift.md) | `POST groups/{groupId}/shifts/{shiftId}` | [docs](https://help.xmatters.com/xmapi/index.html#update-a-shift) |
| [Update form recipients](actions/update-form-recipients.md) | `PUT forms/{formId}/recipients` | [docs](https://help.xmatters.com/xmapi/index.html#update-form-recipients) |
| [Update sender permissions](actions/update-sender-permissions.md) | `PUT forms/{formId}/sender-permissions` | [docs](https://help.xmatters.com/xmapi/index.html#update-sender-permissions) |
| [Upload a User Upload file](actions/upload-a-user-upload-file.md) | `POST uploads/{uploadId}` | [docs](https://help.xmatters.com/xmapi/index.html#upload-a-user-upload-file) |
| [Upload an attachment](actions/upload-an-attachment.md) | `POST attachments` | [docs](https://help.xmatters.com/xmapi/index.html#upload-an-attachment) |
| [Upload an EPIC ZipSync file](actions/upload-an-epic-zip-sync-file.md) | `POST uploads/{uploadId}` | [docs](https://help.xmatters.com/xmapi/index.html#upload-an-epic-zipsync-file) |
| [Upload attachment to a scenario](actions/upload-attachment-to-a-scenario.md) | `POST forms/{formId}/scenarios/{scenarioId}/attachments` | [docs](https://help.xmatters.com/xmapi/index.html#upload-attachment-to-a-scenario) |
