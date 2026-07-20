# <img src="https://images.mindcloud.co/apps/icons/images-1_1775497307230.png" alt="xMatters logo" width="28" height="28"> xMatters: Universal API

Manage incidents, alerts, people, and on-call schedules

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/xMatters/latest
- **Category:** IT Operations / IT Service Management
- **Actions:** 164
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.xmatters.com
- **Vendor API docs:** https://help.xmatters.com/xmapi/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get People](actions/get-people.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (164)

### Annotation

| Action | Method | Description |
| --- | --- | --- |
| [Add a comment to an event](actions/add-a-comment-to-an-event.md) | POST | Adds a comment to an event in your xMatters instance. |
| [Get an event annotation](actions/get-an-event-annotation.md) | GET | Retrieves an event annotation from your xMatters instance. |
| [Get event annotations](actions/get-event-annotations.md) | GET | Retrieves event annotations from your xMatters instance. |

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Get a scenario attachment](actions/get-a-scenario-attachment.md) | GET | Retrieves a scenario attachment from your xMatters instance. |
| [Get a scheduled message attachment](actions/get-a-scheduled-message-attachment.md) | GET | Retrieves a scheduled message attachment from your xMatters instance. |
| [Get an event attachment](actions/get-an-event-attachment.md) | GET | Retrieves an event attachment from your xMatters instance. |
| [Upload an attachment](actions/upload-an-attachment.md) | POST | Uploads an attachment to your xMatters instance. |
| [Upload attachment to a scenario](actions/upload-attachment-to-a-scenario.md) | POST | Uploads attachment to a scenario to your xMatters instance. |

### Audit

| Action | Method | Description |
| --- | --- | --- |
| [Get event audit information](actions/get-event-audit-information.md) | GET | Retrieves event audit information from your xMatters instance. |

### Change

| Action | Method | Description |
| --- | --- | --- |
| [Create a change record](actions/create-a-change-record.md) | POST | Creates a change record in your xMatters instance. |
| [Get a change](actions/get-a-change.md) | GET | Retrieves a change from your xMatters instance. |
| [Get changes](actions/get-changes.md) | GET | Retrieves changes from your xMatters instance. |

### Conference Bridge

| Action | Method | Description |
| --- | --- | --- |
| [Create an external conference bridge](actions/create-an-external-conference-bridge.md) | POST | Creates an external conference bridge in your xMatters instance. |
| [Delete a conference bridge](actions/delete-a-conference-bridge.md) | DELETE | Deletes a conference bridge from your xMatters instance. |
| [Get a conference bridge](actions/get-a-conference-bridge.md) | GET | Retrieves a conference bridge from your xMatters instance. |
| [Get conference bridges](actions/get-conference-bridges.md) | GET | Retrieves conference bridges from your xMatters instance. |
| [Modify a conference bridge](actions/modify-a-conference-bridge.md) | PUT | Updates a conference bridge in your xMatters instance. |

### Constant

| Action | Method | Description |
| --- | --- | --- |
| [Create a plan constant](actions/create-a-plan-constant.md) | POST | Creates a plan constant in your xMatters instance. |
| [Delete a plan constant](actions/delete-a-plan-constant.md) | DELETE | Deletes a plan constant from your xMatters instance. |
| [Get plan constants](actions/get-plan-constants.md) | GET | Retrieves plan constants from your xMatters instance. |
| [Modify a plan constant](actions/modify-a-plan-constant.md) | PUT | Updates a plan constant in your xMatters instance. |

### Device

| Action | Method | Description |
| --- | --- | --- |
| [Create a device](actions/create-a-device.md) | POST | Creates a device in your xMatters instance. |
| [Delete a device](actions/delete-a-device.md) | DELETE | Deletes a device from your xMatters instance. |
| [Get a device](actions/get-a-device.md) | GET | Retrieves a device from your xMatters instance. |
| [Get a person's devices](actions/get-a-person-s-devices.md) | GET | Retrieves a person's devices from your xMatters instance. |
| [Get devices](actions/get-devices.md) | GET | Retrieves devices from your xMatters instance. |
| [Modify a device](actions/modify-a-device.md) | PUT | Updates a device in your xMatters instance. |

### Device Name

| Action | Method | Description |
| --- | --- | --- |
| [Create a device name](actions/create-a-device-name.md) | POST | Creates a device name in your xMatters instance. |
| [Delete a device name](actions/delete-a-device-name.md) | DELETE | Deletes a device name from your xMatters instance. |
| [Get device names](actions/get-device-names.md) | GET | Retrieves device names from your xMatters instance. |
| [Modify a device name](actions/modify-a-device-name.md) | PUT | Updates a device name in your xMatters instance. |

### Device Type

| Action | Method | Description |
| --- | --- | --- |
| [Get device types](actions/get-device-types.md) | GET | Retrieves device types from your xMatters instance. |

### Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Create plan endpoint](actions/create-plan-endpoint.md) | POST | Creates plan endpoint in your xMatters instance. |
| [Delete a plan endpoint](actions/delete-a-plan-endpoint.md) | DELETE | Deletes a plan endpoint from your xMatters instance. |
| [Get plan endpoints](actions/get-plan-endpoints.md) | GET | Retrieves plan endpoints from your xMatters instance. |
| [Modify a plan endpoint](actions/modify-a-plan-endpoint.md) | PUT | Updates a plan endpoint in your xMatters instance. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Change the status of an event](actions/change-the-status-of-an-event.md) | PUT | Changes the status of an event in your xMatters instance. |
| [Get an event](actions/get-an-event.md) | GET | Retrieves an event from your xMatters instance. |
| [Get events](actions/get-events.md) | GET | Retrieves events from your xMatters instance. |

### Event Suppression

| Action | Method | Description |
| --- | --- | --- |
| [Get suppressed events](actions/get-suppressed-events.md) | GET | Retrieves suppressed events from your xMatters instance. |

### Exclusion

| Action | Method | Description |
| --- | --- | --- |
| [Get deleted shift occurrences](actions/get-deleted-shift-occurrences.md) | GET | Retrieves deleted shift occurrences from your xMatters instance. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Create a plan form](actions/create-a-plan-form.md) | POST | Creates a plan form in your xMatters instance. |
| [Get a form in a plan](actions/get-a-form-in-a-plan.md) | GET | Retrieves a form in a plan from your xMatters instance. |
| [Get forms](actions/get-forms.md) | GET | Retrieves forms from your xMatters instance. |
| [Get forms in a plan](actions/get-forms-in-a-plan.md) | GET | Retrieves forms in a plan from your xMatters instance. |
| [Modify a plan form](actions/modify-a-plan-form.md) | PUT | Updates a plan form in your xMatters instance. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create a group](actions/create-a-group.md) | POST | Creates a group in your xMatters instance. |
| [Delete a group](actions/delete-a-group.md) | DELETE | Deletes a group from your xMatters instance. |
| [Get a group](actions/get-a-group.md) | GET | Retrieves a group from your xMatters instance. |
| [Get groups](actions/get-groups.md) | GET | Retrieves groups from your xMatters instance. |
| [Modify a group](actions/modify-a-group.md) | PUT | Updates a group in your xMatters instance. |

### Group Membership

| Action | Method | Description |
| --- | --- | --- |
| [Get a person's groups](actions/get-a-person-s-groups.md) | GET | Retrieves a person's groups from your xMatters instance. |

### Import

| Action | Method | Description |
| --- | --- | --- |
| [Get an import job](actions/get-an-import-job.md) | GET | Retrieves an import job from your xMatters instance. |
| [Get import jobs](actions/get-import-jobs.md) | GET | Retrieves import jobs from your xMatters instance. |

### Import Message

| Action | Method | Description |
| --- | --- | --- |
| [Get import job messages](actions/get-import-job-messages.md) | GET | Retrieves import job messages from your xMatters instance. |

### Incident

| Action | Method | Description |
| --- | --- | --- |
| [Create an incident](actions/create-an-incident.md) | POST | Creates an incident in your xMatters instance. |
| [Get an incident](actions/get-an-incident.md) | GET | Retrieves an incident from your xMatters instance. |
| [Get incidents](actions/get-incidents.md) | GET | Retrieves incidents from your xMatters instance. |
| [Modify an incident](actions/modify-an-incident.md) | PUT | Updates an incident in your xMatters instance. |

### Integration

| Action | Method | Description |
| --- | --- | --- |
| [Create an integration](actions/create-an-integration.md) | POST | Creates an integration in your xMatters instance. |
| [Delete an integration](actions/delete-an-integration.md) | DELETE | Deletes an integration from your xMatters instance. |
| [Get an integration](actions/get-an-integration.md) | GET | Retrieves an integration from your xMatters instance. |
| [Get integrations](actions/get-integrations.md) | GET | Retrieves integrations from your xMatters instance. |
| [Modify an Integration](actions/modify-an-integration.md) | PUT | Updates an Integration in your xMatters instance. |

### License Quota

| Action | Method | Description |
| --- | --- | --- |
| [Get group license quotas](actions/get-group-license-quotas.md) | GET | Retrieves group license quotas from your xMatters instance. |
| [Get user license quotas](actions/get-user-license-quotas.md) | GET | Retrieves user license quotas from your xMatters instance. |

### Log

| Action | Method | Description |
| --- | --- | --- |
| [Get integration logs](actions/get-integration-logs.md) | GET | Retrieves integration logs from your xMatters instance. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Add a member to a shift](actions/add-a-member-to-a-shift.md) | POST | Adds a member to a shift in your xMatters instance. |
| [Add a member to the group](actions/add-a-member-to-the-group.md) | POST | Adds a member to the group in your xMatters instance. |
| [Get group members](actions/get-group-members.md) | GET | Retrieves group members from your xMatters instance. |
| [Get members in a shift](actions/get-members-in-a-shift.md) | GET | Retrieves members in a shift from your xMatters instance. |
| [Remove a member from the group](actions/remove-a-member-from-the-group.md) | DELETE | Removes a member from the group from your xMatters instance. |

### Message Template

| Action | Method | Description |
| --- | --- | --- |
| [Create form message templates](actions/create-form-message-templates.md) | POST | Creates form message templates in your xMatters instance. |
| [Modify a form message template](actions/modify-a-form-message-template.md) | PUT | Updates a form message template in your xMatters instance. |

### Occurrence

| Action | Method | Description |
| --- | --- | --- |
| [Get shift occurrences](actions/get-shift-occurrences.md) | GET | Retrieves shift occurrences from your xMatters instance. |
| [Restore deleted shift occurrences](actions/restore-deleted-shift-occurrences.md) | POST | Restores deleted shift occurrences in your xMatters instance. |

### On Call

| Action | Method | Description |
| --- | --- | --- |
| [Get on-call summary](actions/get-on-call-summary.md) | GET | Retrieves on-call summary from your xMatters instance. |
| [Get who is on call](actions/get-who-is-on-call.md) | GET | Retrieves who is on call from your xMatters instance. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Create a person](actions/create-a-person.md) | POST | Creates a person in your xMatters instance. |
| [Delete a person](actions/delete-a-person.md) | DELETE | Deletes a person from your xMatters instance. |
| [Get a person (by id)](actions/get-a-person-by-id.md) | GET | Retrieves a person by ID from your xMatters instance. |
| [Get People](actions/get-people.md) | GET | Retrieves people from your xMatters instance. |
| [Modify a person](actions/modify-a-person.md) | PUT | Updates a person in your xMatters instance. |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [Create a communication plan](actions/create-a-communication-plan.md) | POST | Creates a communication plan in your xMatters instance. |
| [Delete a plan](actions/delete-a-plan.md) | DELETE | Deletes a plan from your xMatters instance. |
| [Get a communication plan](actions/get-a-communication-plan.md) | GET | Retrieves a communication plan from your xMatters instance. |
| [Get communication plans](actions/get-communication-plans.md) | GET | Retrieves communication plans from your xMatters instance. |
| [Modify communication plan](actions/modify-communication-plan.md) | PUT | Updates communication plan in your xMatters instance. |

### Property Definition

| Action | Method | Description |
| --- | --- | --- |
| [Create plan properties](actions/create-plan-properties.md) | POST | Creates plan properties in your xMatters instance. |
| [Get plan properties](actions/get-plan-properties.md) | GET | Retrieves plan properties from your xMatters instance. |
| [Modify plan properties](actions/modify-plan-properties.md) | PUT | Updates plan properties in your xMatters instance. |

### Recipient

| Action | Method | Description |
| --- | --- | --- |
| [Get a group's recipients](actions/get-a-group-s-recipients.md) | GET | Retrieves a group's recipients from your xMatters instance. |
| [Update form recipients](actions/update-form-recipients.md) | PUT | Updates form recipients in your xMatters instance. |

### Response Option

| Action | Method | Description |
| --- | --- | --- |
| [Create form response options](actions/create-form-response-options.md) | POST | Creates form response options in your xMatters instance. |
| [Get form response options](actions/get-form-response-options.md) | GET | Retrieves form response options from your xMatters instance. |
| [Modify a form response option](actions/modify-a-form-response-option.md) | PUT | Updates a form response option in your xMatters instance. |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [Get roles](actions/get-roles.md) | GET | Retrieves roles from your xMatters instance. |

### Scenario

| Action | Method | Description |
| --- | --- | --- |
| [Create a scenario](actions/create-a-scenario.md) | POST | Creates a scenario in your xMatters instance. |
| [Get a scenario](actions/get-a-scenario.md) | GET | Retrieves a scenario from your xMatters instance. |
| [Get scenarios](actions/get-scenarios.md) | GET | Retrieves scenarios from your xMatters instance. |
| [Get scenarios in a form](actions/get-scenarios-in-a-form.md) | GET | Retrieves scenarios in a form from your xMatters instance. |
| [Modify a scenario](actions/modify-a-scenario.md) | PUT | Updates a scenario in your xMatters instance. |

### Scheduled Message

| Action | Method | Description |
| --- | --- | --- |
| [Create a scheduled message](actions/create-a-scheduled-message.md) | POST | Creates a scheduled message in your xMatters instance. |
| [Delete a scheduled message](actions/delete-a-scheduled-message.md) | DELETE | Deletes a scheduled message from your xMatters instance. |
| [Get a scheduled message](actions/get-a-scheduled-message.md) | GET | Retrieves a scheduled message from your xMatters instance. |
| [Get scheduled messages](actions/get-scheduled-messages.md) | GET | Retrieves scheduled messages from your xMatters instance. |
| [Modify a scheduled message](actions/modify-a-scheduled-message.md) | PUT | Updates a scheduled message in your xMatters instance. |

### Section

| Action | Method | Description |
| --- | --- | --- |
| [Create a form section](actions/create-a-form-section.md) | POST | Creates a form section in your xMatters instance. |
| [Get form sections](actions/get-form-sections.md) | GET | Retrieves form sections from your xMatters instance. |
| [Modify a form section](actions/modify-a-form-section.md) | PUT | Updates a form section in your xMatters instance. |

### Sender Permission

| Action | Method | Description |
| --- | --- | --- |
| [Get scenario sender permissions](actions/get-scenario-sender-permissions.md) | GET | Retrieves scenario sender permissions from your xMatters instance. |
| [Set scenario sender permissions](actions/set-scenario-sender-permissions.md) | PUT | Sets scenario sender permissions in your xMatters instance. |
| [Update sender permissions](actions/update-sender-permissions.md) | PUT | Updates sender permissions in your xMatters instance. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Create a service](actions/create-a-service.md) | POST | Creates a service in your xMatters instance. |
| [Delete a service](actions/delete-a-service.md) | DELETE | Deletes a service from your xMatters instance. |
| [Get a service](actions/get-a-service.md) | GET | Retrieves a service from your xMatters instance. |
| [Get services](actions/get-services.md) | GET | Retrieves services from your xMatters instance. |
| [Modify a service](actions/modify-a-service.md) | PUT | Updates a service in your xMatters instance. |

### Service Dependency

| Action | Method | Description |
| --- | --- | --- |
| [Create a service dependency](actions/create-a-service-dependency.md) | POST | Creates a service dependency in your xMatters instance. |
| [Delete a service dependency](actions/delete-a-service-dependency.md) | DELETE | Deletes a service dependency from your xMatters instance. |
| [Get service dependencies](actions/get-service-dependencies.md) | GET | Retrieves service dependencies from your xMatters instance. |
| [Modify a service dependency](actions/modify-a-service-dependency.md) | PUT | Updates a service dependency in your xMatters instance. |

### Share Permission

| Action | Method | Description |
| --- | --- | --- |
| [Get subscription share permissions](actions/get-subscription-share-permissions.md) | GET | Retrieves subscription share permissions from your xMatters instance. |
| [Set subscription share permissions](actions/set-subscription-share-permissions.md) | PUT | Sets subscription share permissions in your xMatters instance. |

### Shared Library

| Action | Method | Description |
| --- | --- | --- |
| [Create a shared library](actions/create-a-shared-library.md) | POST | Creates a shared library in your xMatters instance. |
| [Delete a shared library](actions/delete-a-shared-library.md) | DELETE | Deletes a shared library from your xMatters instance. |
| [Get a shared library](actions/get-a-shared-library.md) | GET | Retrieves a shared library from your xMatters instance. |
| [Get shared libraries](actions/get-shared-libraries.md) | GET | Retrieves shared libraries from your xMatters instance. |
| [Modify a shared library](actions/modify-a-shared-library.md) | PUT | Updates a shared library in your xMatters instance. |

### Shift

| Action | Method | Description |
| --- | --- | --- |
| [Create a shift](actions/create-a-shift.md) | POST | Creates a shift in your xMatters instance. |
| [Delete a shift](actions/delete-a-shift.md) | DELETE | Deletes a shift from your xMatters instance. |
| [Get a shift](actions/get-a-shift.md) | GET | Retrieves a shift from your xMatters instance. |
| [Get shifts](actions/get-shifts.md) | GET | Retrieves shifts from your xMatters instance. |
| [Update a shift](actions/update-a-shift.md) | PUT | Updates a shift in your xMatters instance. |

### Signal

| Action | Method | Description |
| --- | --- | --- |
| [Get a signal](actions/get-a-signal.md) | GET | Retrieves a signal from your xMatters instance. |
| [Get signals](actions/get-signals.md) | GET | Retrieves signals from your xMatters instance. |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Create a site](actions/create-a-site.md) | POST | Creates a site in your xMatters instance. |
| [Delete a site](actions/delete-a-site.md) | DELETE | Deletes a site from your xMatters instance. |
| [Get a site](actions/get-a-site.md) | GET | Retrieves a site from your xMatters instance. |
| [Get sites](actions/get-sites.md) | GET | Retrieves sites from your xMatters instance. |
| [Modify a site](actions/modify-a-site.md) | PUT | Updates a site in your xMatters instance. |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [Add subscribers](actions/add-subscribers.md) | POST | Adds subscribers in your xMatters instance. |
| [Get subscribers](actions/get-subscribers.md) | GET | Retrieves subscribers from your xMatters instance. |
| [Unsubscribe a user](actions/unsubscribe-a-user.md) | DELETE | Unsubscribes a user from your xMatters instance. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create a subscription](actions/create-a-subscription.md) | POST | Creates a subscription in your xMatters instance. |
| [Delete a subscription](actions/delete-a-subscription.md) | DELETE | Deletes a subscription from your xMatters instance. |
| [Get a subscription](actions/get-a-subscription.md) | GET | Retrieves a subscription from your xMatters instance. |
| [Get subscriptions](actions/get-subscriptions.md) | GET | Retrieves subscriptions from your xMatters instance. |
| [Modify a subscription](actions/modify-a-subscription.md) | PUT | Updates a subscription in your xMatters instance. |

### Subscription Form

| Action | Method | Description |
| --- | --- | --- |
| [Create a subscription form](actions/create-a-subscription-form.md) | POST | Creates a subscription form in your xMatters instance. |
| [Get a subscription form](actions/get-a-subscription-form.md) | GET | Retrieves a subscription form from your xMatters instance. |
| [Get subscription forms](actions/get-subscription-forms.md) | GET | Retrieves subscription forms from your xMatters instance. |
| [Get subscription forms in a plan](actions/get-subscription-forms-in-a-plan.md) | GET | Retrieves subscription forms in a plan from your xMatters instance. |
| [Modify a subscription form](actions/modify-a-subscription-form.md) | PUT | Updates a subscription form in your xMatters instance. |

### Supervisor

| Action | Method | Description |
| --- | --- | --- |
| [Get a group's supervisors](actions/get-a-group-s-supervisors.md) | GET | Retrieves a group's supervisors from your xMatters instance. |
| [Get a person's supervisors](actions/get-a-person-s-supervisors.md) | GET | Retrieves a person's supervisors from your xMatters instance. |

### Temporary Absence

| Action | Method | Description |
| --- | --- | --- |
| [Create a temporary absence](actions/create-a-temporary-absence.md) | POST | Creates a temporary absence in your xMatters instance. |
| [Delete a temporary absence](actions/delete-a-temporary-absence.md) | DELETE | Deletes a temporary absence from your xMatters instance. |
| [Get temporary absences](actions/get-temporary-absences.md) | GET | Retrieves temporary absences from your xMatters instance. |

### Timeline Entry

| Action | Method | Description |
| --- | --- | --- |
| [Add a timeline note](actions/add-a-timeline-note.md) | POST | Adds a timeline note in your xMatters instance. |

### Trigger

| Action | Method | Description |
| --- | --- | --- |
| [Trigger an incident](actions/trigger-an-incident.md) | POST | Triggers an incident in your xMatters instance. |

### Upload

| Action | Method | Description |
| --- | --- | --- |
| [Upload a User Upload file](actions/upload-a-user-upload-file.md) | POST | Uploads a User Upload file to your xMatters instance. |
| [Upload an EPIC ZipSync file](actions/upload-an-epic-zip-sync-file.md) | POST | Uploads an EPIC ZipSync file to your xMatters instance. |

### User Delivery

| Action | Method | Description |
| --- | --- | --- |
| [Get user delivery data](actions/get-user-delivery-data.md) | GET | Retrieves user delivery data from your xMatters instance. |

