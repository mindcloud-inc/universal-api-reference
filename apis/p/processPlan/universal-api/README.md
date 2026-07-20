# <img src="https://images.mindcloud.co/apps/icons/process-plan_1775825032017.png" alt="Process Plan logo" width="28" height="28"> Process Plan: Universal API

Manage business processes, tasks, tables, and automation

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/processPlan/latest
- **Category:** Productivity / Project Management
- **Actions:** 661
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://processplan.com
- **Vendor API docs:** https://answers.processplan.com/c/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Process Instance Field](actions/get-process-instance-field.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-process-instance-field?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (661)

### Account Management

| Action | Method | Description |
| --- | --- | --- |
| [Delete Dark Background Logo for Accounts](actions/delete-dark-background-logo-for-accounts.md) | DELETE |  |
| [Delete Light Background Logo for Accounts](actions/delete-light-background-logo-for-accounts.md) | DELETE |  |
| [Get Account](actions/get-account.md) | GET |  |
| [Update Account](actions/update-account.md) | PUT |  |
| [Update Account Plan](actions/update-account-plan.md) | PUT |  |
| [Update Dark Background Logo for Accounts](actions/update-dark-background-logo-for-accounts.md) | PUT |  |
| [Update Light Background Logo for Accounts](actions/update-light-background-logo-for-accounts.md) | PUT |  |

### Audit Log

| Action | Method | Description |
| --- | --- | --- |
| [List Audit Entries](actions/list-audit-entries.md) | GET |  |
| [List Audit Entries for Process Instance Header](actions/list-audit-entries-for-process-instance-header.md) | GET |  |
| [List Audit Entries for Process Template Header](actions/list-audit-entries-for-process-template-header.md) | GET |  |
| [List Audit Entries for Proxy Job](actions/list-audit-entries-for-proxy-job.md) | GET |  |
| [List Audit Entries for Proxy Run](actions/list-audit-entries-for-proxy-run.md) | GET |  |
| [List Audit Entries for User](actions/list-audit-entries-for-user.md) | GET |  |
| [List Audit Entries for User Group](actions/list-audit-entries-for-user-group.md) | GET |  |

### Automated Action

| Action | Method | Description |
| --- | --- | --- |
| [Count Automated Actions for Process Template Header](actions/count-automated-actions-for-process-template-header.md) | GET |  |
| [Create Automated Action for Process Template Header](actions/create-automated-action-for-process-template-header.md) | POST |  |
| [Delete Automated Action](actions/delete-automated-action.md) | DELETE |  |
| [Duplicate Automated Action](actions/duplicate-automated-action.md) | POST |  |
| [Get Automated Action](actions/get-automated-action.md) | GET |  |
| [Get Start Date for Scheduleds in Automated Action Calculate Nexts](actions/get-start-date-for-scheduleds-in-automated-action-calculate-nexts.md) | POST |  |
| [List Active Automated Actions for Process Template Header](actions/list-active-automated-actions-for-process-template-header.md) | GET |  |
| [List Automated Actions](actions/list-automated-actions.md) | GET |  |
| [List Automated Actions for Process Template Header](actions/list-automated-actions-for-process-template-header.md) | GET |  |
| [List Automated Actions for Process Template Task](actions/list-automated-actions-for-process-template-task.md) | GET |  |
| [List Automated Actions for Process Template Task Response](actions/list-automated-actions-for-process-template-task-response.md) | GET |  |
| [Search Automated Actions for Process Template Header](actions/search-automated-actions-for-process-template-header.md) | GET |  |
| [Update Automated Action](actions/update-automated-action.md) | PUT |  |

### Automated Action Condition

| Action | Method | Description |
| --- | --- | --- |
| [Count Automated Action Conditions for Automated Action](actions/count-automated-action-conditions-for-automated-action.md) | GET |  |
| [Create Automated Action Condition for Automated Action](actions/create-automated-action-condition-for-automated-action.md) | POST |  |
| [Delete Automated Action Condition](actions/delete-automated-action-condition.md) | DELETE |  |
| [Delete Automated Action Conditions for Automated Action](actions/delete-automated-action-conditions-for-automated-action.md) | DELETE |  |
| [Get Automated Action Condition](actions/get-automated-action-condition.md) | GET |  |
| [List Automated Action Conditions for Automated Action](actions/list-automated-action-conditions-for-automated-action.md) | GET |  |
| [Update Automated Action Condition](actions/update-automated-action-condition.md) | PUT |  |

### Automated Action Property

| Action | Method | Description |
| --- | --- | --- |
| [Count Automated Action Properties for Automated Action](actions/count-automated-action-properties-for-automated-action.md) | GET |  |
| [Create Automated Action Property for Automated Action](actions/create-automated-action-property-for-automated-action.md) | POST |  |
| [Delete Automated Action Property](actions/delete-automated-action-property.md) | DELETE |  |
| [Get Automated Action Property](actions/get-automated-action-property.md) | GET |  |
| [List Active Automated Action Properties for Process Proxy Job](actions/list-active-automated-action-properties-for-process-proxy-job.md) | GET |  |
| [List Automated Action Properties for Automated Action](actions/list-automated-action-properties-for-automated-action.md) | GET |  |
| [Refresh Automated Action Properties for Automated Action](actions/refresh-automated-action-properties-for-automated-action.md) | PUT |  |
| [Search Automated Action Properties for Automated Action](actions/search-automated-action-properties-for-automated-action.md) | GET |  |
| [Update Automated Action Property](actions/update-automated-action-property.md) | PUT |  |

### Csv Import Template

| Action | Method | Description |
| --- | --- | --- |
| [Count CSV Import Templates](actions/count-csv-import-templates.md) | GET |  |
| [Create CSV Import Template for Process Template Header](actions/create-csv-import-template-for-process-template-header.md) | POST |  |
| [Delete CSV Import Template](actions/delete-csv-import-template.md) | DELETE |  |
| [Get CSV Import Template](actions/get-csv-import-template.md) | GET |  |
| [List CSV Import Templates](actions/list-csv-import-templates.md) | GET |  |
| [List CSV Import Templates for Process Template Header](actions/list-csv-import-templates-for-process-template-header.md) | GET |  |
| [Start Process Instance Header for CSV Import Template](actions/start-process-instance-header-for-csv-import-template.md) | POST |  |
| [Update CSV Import Template](actions/update-csv-import-template.md) | PUT |  |

### Csv Import Template Field Mapping

| Action | Method | Description |
| --- | --- | --- |
| [Create Field Mapping for CSV Import Templates in CSV Import Template](actions/create-field-mapping-for-csv-import-templates-in-csv-import-template.md) | POST |  |
| [Delete Field Mapping for CSV Import Templates](actions/delete-field-mapping-for-csv-import-templates.md) | DELETE |  |
| [Get Field Mapping for CSV Import Templates](actions/get-field-mapping-for-csv-import-templates.md) | GET |  |
| [Get Field Mapping for CSV Import Templates in Process Template Field in CSV Import Template](actions/get-field-mapping-for-csv-import-templates-in-process-template-field-in-csv-import-template.md) | GET |  |
| [List Field Mappings for CSV Import Templates in CSV Import Template](actions/list-field-mappings-for-csv-import-templates-in-csv-import-template.md) | GET |  |
| [Search Field Mappings for CSV Import Templates in CSV Import Template](actions/search-field-mappings-for-csv-import-templates-in-csv-import-template.md) | GET |  |
| [Update Field Mapping for CSV Import Templates](actions/update-field-mapping-for-csv-import-templates.md) | PUT |  |

### Custom Api Connection

| Action | Method | Description |
| --- | --- | --- |
| [Convert Custom API Connections IDs to Objects](actions/convert-custom-api-connections-i-ds-to-objects.md) | GET |  |
| [Count Custom API Connections](actions/count-custom-api-connections.md) | GET |  |
| [Create Custom API Connection](actions/create-custom-api-connection.md) | POST |  |
| [Delete Custom API Connection](actions/delete-custom-api-connection.md) | DELETE |  |
| [Delete Custom API Connections](actions/delete-custom-api-connections.md) | DELETE |  |
| [Get Custom API Connection](actions/get-custom-api-connection.md) | GET |  |
| [Get Test Connection for Custom API Connection](actions/get-test-connection-for-custom-api-connection.md) | POST |  |
| [List Custom API Connections](actions/list-custom-api-connections.md) | GET |  |
| [List Custom API Connections As Text Values](actions/list-custom-api-connections-as-text-values.md) | GET |  |
| [Update Custom API Connection](actions/update-custom-api-connection.md) | PUT |  |

### Custom Api Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Convert Custom API Endpoints IDs to Objects](actions/convert-custom-api-endpoints-i-ds-to-objects.md) | GET |  |
| [Count Custom API Endpoints](actions/count-custom-api-endpoints.md) | GET |  |
| [Create Custom API Endpoint](actions/create-custom-api-endpoint.md) | POST |  |
| [Delete Custom API Endpoint](actions/delete-custom-api-endpoint.md) | DELETE |  |
| [Delete Custom API Endpoints](actions/delete-custom-api-endpoints.md) | DELETE |  |
| [Get Custom API Endpoint](actions/get-custom-api-endpoint.md) | GET |  |
| [Get Result As Text Value for Custom API Endpoint in Process Template Header](actions/get-result-as-text-value-for-custom-api-endpoint-in-process-template-header.md) | GET |  |
| [List Custom API Endpoints](actions/list-custom-api-endpoints.md) | GET |  |
| [List Custom API Endpoints As Text Values](actions/list-custom-api-endpoints-as-text-values.md) | GET |  |
| [Update Custom API Endpoint](actions/update-custom-api-endpoint.md) | PUT |  |

### Data Query

| Action | Method | Description |
| --- | --- | --- |
| [Convert Data Queries IDs to Objects](actions/convert-data-queries-i-ds-to-objects.md) | GET |  |
| [Count Data Queries](actions/count-data-queries.md) | GET |  |
| [Create Data Query](actions/create-data-query.md) | POST |  |
| [Delete Data Queries](actions/delete-data-queries.md) | DELETE |  |
| [Delete Data Query](actions/delete-data-query.md) | DELETE |  |
| [Get Data Query](actions/get-data-query.md) | GET |  |
| [Get Result As Text Value for Data Query in Process Template Header](actions/get-result-as-text-value-for-data-query-in-process-template-header.md) | GET |  |
| [List Data Queries](actions/list-data-queries.md) | GET |  |
| [List Data Queries As Text Values](actions/list-data-queries-as-text-values.md) | GET |  |
| [Update Data Query](actions/update-data-query.md) | PUT |  |

### Data Source

| Action | Method | Description |
| --- | --- | --- |
| [Convert Data Sources IDs to Objects](actions/convert-data-sources-i-ds-to-objects.md) | GET |  |
| [Count Data Sources](actions/count-data-sources.md) | GET |  |
| [Create Data Source](actions/create-data-source.md) | POST |  |
| [Delete Data Source](actions/delete-data-source.md) | DELETE |  |
| [Delete Data Sources](actions/delete-data-sources.md) | DELETE |  |
| [Get Data Source](actions/get-data-source.md) | GET |  |
| [Get Test Connection for Data Source](actions/get-test-connection-for-data-source.md) | POST |  |
| [List Data Sources](actions/list-data-sources.md) | GET |  |
| [List Data Sources As Text Values](actions/list-data-sources-as-text-values.md) | GET |  |
| [Update Data Source](actions/update-data-source.md) | PUT |  |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Create File](actions/create-file.md) | POST |  |
| [Delete File](actions/delete-file.md) | DELETE |  |
| [Get File](actions/get-file.md) | GET |  |
| [Refresh Private URL for File](actions/refresh-private-url-for-file.md) | GET |  |
| [Update File](actions/update-file.md) | PUT |  |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Count Messages](actions/count-messages.md) | GET |  |
| [Count Unread Messages for Message Thread](actions/count-unread-messages-for-message-thread.md) | GET |  |
| [Count Unread Messages for Process Instance Header](actions/count-unread-messages-for-process-instance-header.md) | GET |  |
| [Count Unread Messages for Process Template Header](actions/count-unread-messages-for-process-template-header.md) | GET |  |
| [Create Message](actions/create-message.md) | POST |  |
| [Delete Message](actions/delete-message.md) | DELETE |  |
| [Get Message](actions/get-message.md) | GET |  |
| [List Messages for Message Thread](actions/list-messages-for-message-thread.md) | GET |  |
| [List Messages for Process Instance Header](actions/list-messages-for-process-instance-header.md) | GET |  |
| [List Messages for Process Template Header](actions/list-messages-for-process-template-header.md) | GET |  |
| [List Messages With Process Instance Header Messages for Process Template Header](actions/list-messages-with-process-instance-header-messages-for-process-template-header.md) | GET |  |
| [Update Message](actions/update-message.md) | PUT |  |

### Message File

| Action | Method | Description |
| --- | --- | --- |
| [Apply File for Message](actions/apply-file-for-message.md) | PUT |  |
| [Count Files for Message](actions/count-files-for-message.md) | GET |  |
| [Get File for Message](actions/get-file-for-message.md) | GET |  |
| [List Files for Message](actions/list-files-for-message.md) | GET |  |
| [Remove File for Message](actions/remove-file-for-message.md) | DELETE |  |

### Message Thread

| Action | Method | Description |
| --- | --- | --- |
| [Convert Message Threads IDs to Objects](actions/convert-message-threads-i-ds-to-objects.md) | GET |  |
| [Count Message Threads](actions/count-message-threads.md) | GET |  |
| [Create Message Thread](actions/create-message-thread.md) | POST |  |
| [Delete Message Thread](actions/delete-message-thread.md) | DELETE |  |
| [Delete Message Threads](actions/delete-message-threads.md) | DELETE |  |
| [Get Message Thread](actions/get-message-thread.md) | GET |  |
| [List Message Threads](actions/list-message-threads.md) | GET |  |
| [Update Message Thread](actions/update-message-thread.md) | PUT |  |

### Messages To User

| Action | Method | Description |
| --- | --- | --- |
| [Count Unread Messages for Me](actions/count-unread-messages-for-me.md) | GET |  |
| [Create Message to User for Message](actions/create-message-to-user-for-message.md) | POST |  |
| [Delete Message for Me](actions/delete-message-for-me.md) | DELETE |  |
| [Delete Messages for Me](actions/delete-messages-for-me.md) | DELETE |  |
| [Get Previous Message to User for Process Instance Header](actions/get-previous-message-to-user-for-process-instance-header.md) | GET |  |
| [Get Set Reminder for Message in Me](actions/get-set-reminder-for-message-in-me.md) | POST |  |
| [Get User for Message](actions/get-user-for-message.md) | GET |  |
| [List Message to Users for Message](actions/list-message-to-users-for-message.md) | GET |  |
| [List Messages for Me](actions/list-messages-for-me.md) | GET |  |
| [List Previous Message to Users for Message Channel](actions/list-previous-message-to-users-for-message-channel.md) | GET |  |

### Miscellaneous

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update Process Instances](actions/bulk-update-process-instances.md) | PUT |  |
| [Convert Results IDs to Objects](actions/convert-results-i-ds-to-objects.md) | GET |  |
| [Get Global Search](actions/get-global-search.md) | GET |  |
| [Get Invoice](actions/get-invoice.md) | GET |  |
| [Get Package for Partner](actions/get-package-for-partner.md) | GET |  |
| [List Countries for Miscellaneous Items](actions/list-countries-for-miscellaneous-items.md) | GET |  |
| [List Event Types](actions/list-event-types.md) | GET |  |
| [List Invoices](actions/list-invoices.md) | GET |  |
| [List Languages for Miscellaneous Items](actions/list-languages-for-miscellaneous-items.md) | GET |  |
| [List Timezones for Miscellaneous Items](actions/list-timezones-for-miscellaneous-items.md) | GET |  |
| [List US States for Miscellaneous Items](actions/list-us-states-for-miscellaneous-items.md) | GET |  |
| [Ping](actions/ping.md) | GET |  |

### Process Diagram Link

| Action | Method | Description |
| --- | --- | --- |
| [Count Diagram Links for Version Timestamp in Process Template Header](actions/count-diagram-links-for-version-timestamp-in-process-template-header.md) | GET |  |
| [Count Inbound Links for Process Template Task in Process Instance Header](actions/count-inbound-links-for-process-template-task-in-process-instance-header.md) | GET |  |
| [Count Process Template Task Milestones for Process Template Header](actions/count-process-template-task-milestones-for-process-template-header.md) | GET |  |
| [Delete Diagram Link for Processes](actions/delete-diagram-link-for-processes.md) | DELETE |  |
| [Get Diagram Link for Create Nodes in Message in Process Template Header](actions/get-diagram-link-for-create-nodes-in-message-in-process-template-header.md) | POST |  |
| [Get Diagram Model for Process Instance Header](actions/get-diagram-model-for-process-instance-header.md) | GET |  |
| [Get Diagram Model for Process Instance Heat Map in Process Template Header](actions/get-diagram-model-for-process-instance-heat-map-in-process-template-header.md) | GET |  |
| [Get Diagram Model for Process Template Header](actions/get-diagram-model-for-process-template-header.md) | GET |  |
| [Get Suggestion for Process Instance Task in Process Template Header Diagram Model](actions/get-suggestion-for-process-instance-task-in-process-template-header-diagram-model.md) | GET |  |
| [List Diagram Links for Process Template Header](actions/list-diagram-links-for-process-template-header.md) | GET |  |
| [List Process Instance Tasks With Public Milestones for Process Instance Header](actions/list-process-instance-tasks-with-public-milestones-for-process-instance-header.md) | GET |  |
| [List Process Template Connectors for Process Template Connector in Process Instance Header](actions/list-process-template-connectors-for-process-template-connector-in-process-instance-header.md) | GET |  |
| [List Process Template Connectors for Process Template Task Response in Process Instance Header](actions/list-process-template-connectors-for-process-template-task-response-in-process-instance-header.md) | GET |  |
| [List Process Template Task Responses As Text Values for Process Template Task in Process Template Header](actions/list-process-template-task-responses-as-text-values-for-process-template-task-in-process-template-header.md) | GET |  |
| [List Process Template Task Responses for Process Template Task in Process Instance Header](actions/list-process-template-task-responses-for-process-template-task-in-process-instance-header.md) | GET |  |
| [List Process Template Task Responses for Process Template Task in Process Template Header](actions/list-process-template-task-responses-for-process-template-task-in-process-template-header.md) | GET |  |
| [List Process Template Tasks for Process Template Connector in Process Instance Header](actions/list-process-template-tasks-for-process-template-connector-in-process-instance-header.md) | GET |  |
| [List Process Template Tasks for Process Template Task Response in Process Instance Header](actions/list-process-template-tasks-for-process-template-task-response-in-process-instance-header.md) | GET |  |
| [List Process Template Tasks for Process Template Task Response in Process Template Header](actions/list-process-template-tasks-for-process-template-task-response-in-process-template-header.md) | GET |  |
| [Update Diagram Model for Process Instance Header](actions/update-diagram-model-for-process-instance-header.md) | POST |  |
| [Update Diagram Model for Process Template Header](actions/update-diagram-model-for-process-template-header.md) | POST |  |

### Process Instance Field

| Action | Method | Description |
| --- | --- | --- |
| [Count Process Instance Fields](actions/count-process-instance-fields.md) | GET |  |
| [Count Process Instance Fields for Process Template Field](actions/count-process-instance-fields-for-process-template-field.md) | GET |  |
| [Create Process Instance Field for Process Instance Header](actions/create-process-instance-field-for-process-instance-header.md) | POST |  |
| [Get Most Recent Process Instance Field for Process Template Field](actions/get-most-recent-process-instance-field-for-process-template-field.md) | GET |  |
| [Get Process Instance Field](actions/get-process-instance-field.md) | GET |  |
| [Get Process Instance Field for Process Template Field in Process Instance Header](actions/get-process-instance-field-for-process-template-field-in-process-instance-header.md) | GET |  |
| [List Process Instance Fields](actions/list-process-instance-fields.md) | GET |  |
| [List Process Instance Fields for Process Template Field](actions/list-process-instance-fields-for-process-template-field.md) | GET |  |
| [List Process Instance Headers Date Fields Only for Process Template Field](actions/list-process-instance-headers-date-fields-only-for-process-template-field.md) | GET |  |
| [List Process Instance Headers Date Fields Only for Process Template Header](actions/list-process-instance-headers-date-fields-only-for-process-template-header.md) | GET |  |
| [List Valid Process Instance Fields for Process Template Field](actions/list-valid-process-instance-fields-for-process-template-field.md) | GET |  |
| [Refresh Process Instance Fields for Process Instance Header](actions/refresh-process-instance-fields-for-process-instance-header.md) | PUT |  |
| [Refresh Process Instance Fields for Process Template Header](actions/refresh-process-instance-fields-for-process-template-header.md) | PUT |  |
| [Search Process Instance Fields for Process Instance Header](actions/search-process-instance-fields-for-process-instance-header.md) | GET |  |
| [Update Process Instance Field](actions/update-process-instance-field.md) | PUT |  |

### Process Instance Field File

| Action | Method | Description |
| --- | --- | --- |
| [Apply File for Process Instance Field](actions/apply-file-for-process-instance-field.md) | PUT |  |
| [Count Files for Process Instance Field](actions/count-files-for-process-instance-field.md) | GET |  |
| [Count Process Instance Fields for File](actions/count-process-instance-fields-for-file.md) | GET |  |
| [Create File for Process Instance Field](actions/create-file-for-process-instance-field.md) | POST |  |
| [Get File for Process Instance Field](actions/get-file-for-process-instance-field.md) | GET |  |
| [List Files for Process Instance Field](actions/list-files-for-process-instance-field.md) | GET |  |
| [List Files for Process Instance Header](actions/list-files-for-process-instance-header.md) | GET |  |
| [List Files for Process Instance Headers](actions/list-files-for-process-instance-headers.md) | GET |  |
| [List Files for Process Template Field in Process Instance Header](actions/list-files-for-process-template-field-in-process-instance-header.md) | GET |  |
| [List Process Instance Fields for File](actions/list-process-instance-fields-for-file.md) | GET |  |
| [Remove All Files for Process Template Field in Process Instance Header](actions/remove-all-files-for-process-template-field-in-process-instance-header.md) | POST |  |
| [Remove File for Process Instance Field](actions/remove-file-for-process-instance-field.md) | DELETE |  |

### Process Instance Header

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Next Scheduled Launch Date](actions/calculate-next-scheduled-launch-date.md) | POST |  |
| [Cancel Process Instance Header](actions/cancel-process-instance-header.md) | PUT |  |
| [Cancel Process Instance Headers](actions/cancel-process-instance-headers.md) | PUT |  |
| [Convert Process Instance Headers IDs to Objects](actions/convert-process-instance-headers-i-ds-to-objects.md) | GET |  |
| [Convert Process Instance Headers IDs to Objects for Process Template Header](actions/convert-process-instance-headers-i-ds-to-objects-for-process-template-header.md) | GET |  |
| [Copy Process Instance Header](actions/copy-process-instance-header.md) | POST |  |
| [Count Other Pending Process Instance Headers for Process Template Header](actions/count-other-pending-process-instance-headers-for-process-template-header.md) | GET |  |
| [Count Past Due Process Instance Headers](actions/count-past-due-process-instance-headers.md) | GET |  |
| [Count Past Due Process Instance Headers for Process Template Group](actions/count-past-due-process-instance-headers-for-process-template-group.md) | GET |  |
| [Count Past Due Process Instance Headers for Process Template Header](actions/count-past-due-process-instance-headers-for-process-template-header.md) | GET |  |
| [Count Past Due Process Instance Headers for User Group](actions/count-past-due-process-instance-headers-for-user-group.md) | GET |  |
| [Count Pending Process Instance Headers](actions/count-pending-process-instance-headers.md) | GET |  |
| [Count Pending Process Instance Headers for Process Template Group](actions/count-pending-process-instance-headers-for-process-template-group.md) | GET |  |
| [Count Pending Process Instance Headers for Process Template Header](actions/count-pending-process-instance-headers-for-process-template-header.md) | GET |  |
| [Count Pending Process Instance Headers for User Group](actions/count-pending-process-instance-headers-for-user-group.md) | GET |  |
| [Count Process Instance Headers](actions/count-process-instance-headers.md) | GET |  |
| [Count Process Instance Headers for Process Template Header](actions/count-process-instance-headers-for-process-template-header.md) | GET |  |
| [Count Process Instance Headers With Process Instance Fields for Process Template Header](actions/count-process-instance-headers-with-process-instance-fields-for-process-template-header.md) | GET |  |
| [Create Process Instance Header for Process Template Header](actions/create-process-instance-header-for-process-template-header.md) | POST |  |
| [Delete Process Instance Header](actions/delete-process-instance-header.md) | DELETE |  |
| [Delete Process Instance Headers](actions/delete-process-instance-headers.md) | DELETE |  |
| [Get Full Text Log for Process Instance Header](actions/get-full-text-log-for-process-instance-header.md) | GET |  |
| [Get Primary Document for Process Instance Header](actions/get-primary-document-for-process-instance-header.md) | GET |  |
| [Get Process Instance Header](actions/get-process-instance-header.md) | GET |  |
| [List Canceled Process Instance Headers](actions/list-canceled-process-instance-headers.md) | GET |  |
| [List Completed Process Instance Headers](actions/list-completed-process-instance-headers.md) | GET |  |
| [List Completed Process Instance Headers for Process Template Header](actions/list-completed-process-instance-headers-for-process-template-header.md) | GET |  |
| [List Initiated Process Instance Headers for Process Template Field in Process Instance Header](actions/list-initiated-process-instance-headers-for-process-template-field-in-process-instance-header.md) | GET |  |
| [List Initiated Process Instance Headers With Process Instance Fields for Process Template Field in Process Instance Header](actions/list-initiated-process-instance-headers-with-process-instance-fields-for-process-template-field-in-process-instance-header.md) | GET |  |
| [List Past Due Process Instance Headers](actions/list-past-due-process-instance-headers.md) | GET |  |
| [List Past Due Process Instance Headers for Process Template Group](actions/list-past-due-process-instance-headers-for-process-template-group.md) | GET |  |
| [List Past Due Process Instance Headers for Process Template Header](actions/list-past-due-process-instance-headers-for-process-template-header.md) | GET |  |
| [List Past Due Process Instance Headers for User Group](actions/list-past-due-process-instance-headers-for-user-group.md) | GET |  |
| [List Pending Process Instance Headers](actions/list-pending-process-instance-headers.md) | GET |  |
| [List Pending Process Instance Headers As Text Values](actions/list-pending-process-instance-headers-as-text-values.md) | GET |  |
| [List Pending Process Instance Headers for Process Template Group](actions/list-pending-process-instance-headers-for-process-template-group.md) | GET |  |
| [List Pending Process Instance Headers for Process Template Header](actions/list-pending-process-instance-headers-for-process-template-header.md) | GET |  |
| [List Pending Process Instance Headers for User Group](actions/list-pending-process-instance-headers-for-user-group.md) | GET |  |
| [List Pending Subprocess Instance Headers for Process Instance Header](actions/list-pending-subprocess-instance-headers-for-process-instance-header.md) | GET |  |
| [List Process Edits for Process Instance Header](actions/list-process-edits-for-process-instance-header.md) | GET |  |
| [List Process Instance Headers](actions/list-process-instance-headers.md) | GET |  |
| [List Process Instance Headers As Text Values](actions/list-process-instance-headers-as-text-values.md) | GET |  |
| [List Process Instance Headers As Text Values for Process Template Header](actions/list-process-instance-headers-as-text-values-for-process-template-header.md) | GET |  |
| [List Process Instance Headers for Process Template Header](actions/list-process-instance-headers-for-process-template-header.md) | GET |  |
| [List Process Instance Headers With Primary Document As Text Values](actions/list-process-instance-headers-with-primary-document-as-text-values.md) | GET |  |
| [List Process Instance Headers With Primary Document As Text Values for Process Template Header](actions/list-process-instance-headers-with-primary-document-as-text-values-for-process-template-header.md) | GET |  |
| [List Process Instance Headers With Process Instance Fields](actions/list-process-instance-headers-with-process-instance-fields.md) | GET |  |
| [List Process Instance Headers With Process Instance Fields for Process Template Header](actions/list-process-instance-headers-with-process-instance-fields-for-process-template-header.md) | GET |  |
| [List Process Instance Headers With Published Primary Documents](actions/list-process-instance-headers-with-published-primary-documents.md) | GET |  |
| [List Process Instance Headers With Published Primary Documents for Process Template Header](actions/list-process-instance-headers-with-published-primary-documents-for-process-template-header.md) | GET |  |
| [List Process Instance Headers With Unpublished Primary Documents](actions/list-process-instance-headers-with-unpublished-primary-documents.md) | GET |  |
| [List Process Visibilities for Process Instance Header](actions/list-process-visibilities-for-process-instance-header.md) | GET |  |
| [List Rolled Up Process Instance Fields for Process Template Header](actions/list-rolled-up-process-instance-fields-for-process-template-header.md) | GET |  |
| [List Scheduled Process Instance Headers](actions/list-scheduled-process-instance-headers.md) | GET |  |
| [List Scheduled Process Instance Headers for Process Template Header](actions/list-scheduled-process-instance-headers-for-process-template-header.md) | GET |  |
| [List Similar Process Instance Headers Excluding Process Template Field for Process Template Header](actions/list-similar-process-instance-headers-excluding-process-template-field-for-process-template-header.md) | GET |  |
| [List Subprocess Instance Headers for Process Instance Header](actions/list-subprocess-instance-headers-for-process-instance-header.md) | GET |  |
| [List Valid Process Instance Headers](actions/list-valid-process-instance-headers.md) | GET |  |
| [List Valid Process Instance Headers for Process Template Header](actions/list-valid-process-instance-headers-for-process-template-header.md) | GET |  |
| [Schedule Process Instance Header for Process Template Header](actions/schedule-process-instance-header-for-process-template-header.md) | POST |  |
| [Set Schedule End for Process Instance Header](actions/set-schedule-end-for-process-instance-header.md) | PUT |  |
| [Set Schedule End for Process Instance Headers](actions/set-schedule-end-for-process-instance-headers.md) | PUT |  |
| [Start Scheduled Instance for Process Instance Header](actions/start-scheduled-instance-for-process-instance-header.md) | POST |  |
| [Update Process Instance Header](actions/update-process-instance-header.md) | PUT |  |
| [Update Process Instance Headers](actions/update-process-instance-headers.md) | PUT |  |

### Process Instance Task

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Process Instance Task](actions/cancel-process-instance-task.md) | PUT |  |
| [Cancel Process Instance Tasks](actions/cancel-process-instance-tasks.md) | PUT |  |
| [Cancel Process Template Task for Process Instance Header](actions/cancel-process-template-task-for-process-instance-header.md) | PUT |  |
| [Count Past Due Process Instance Tasks for Me](actions/count-past-due-process-instance-tasks-for-me.md) | GET |  |
| [Count Past Due Process Instance Tasks for Process Template Task](actions/count-past-due-process-instance-tasks-for-process-template-task.md) | GET |  |
| [Count Past Due Process Instance Tasks for User](actions/count-past-due-process-instance-tasks-for-user.md) | GET |  |
| [Count Past Due Process Instance Tasks for User Group](actions/count-past-due-process-instance-tasks-for-user-group.md) | GET |  |
| [Count Pending Personal Instance Tasks for Me](actions/count-pending-personal-instance-tasks-for-me.md) | GET |  |
| [Count Pending Process Instance Tasks for Me](actions/count-pending-process-instance-tasks-for-me.md) | GET |  |
| [Count Pending Process Instance Tasks for Process Instance Header](actions/count-pending-process-instance-tasks-for-process-instance-header.md) | GET |  |
| [Count Pending Process Instance Tasks for Process Template Header](actions/count-pending-process-instance-tasks-for-process-template-header.md) | GET |  |
| [Count Pending Process Instance Tasks for Process Template Task](actions/count-pending-process-instance-tasks-for-process-template-task.md) | GET |  |
| [Count Pending Process Instance Tasks for User](actions/count-pending-process-instance-tasks-for-user.md) | GET |  |
| [Count Pending Process Instance Tasks for User Group](actions/count-pending-process-instance-tasks-for-user-group.md) | GET |  |
| [Count Process Instance Tasks Completed Today for Me](actions/count-process-instance-tasks-completed-today-for-me.md) | GET |  |
| [Count Process Instance Tasks Completed Today for User](actions/count-process-instance-tasks-completed-today-for-user.md) | GET |  |
| [Count Process Instance Tasks Due This Week for Me](actions/count-process-instance-tasks-due-this-week-for-me.md) | GET |  |
| [Count Process Instance Tasks Due This Week for User](actions/count-process-instance-tasks-due-this-week-for-user.md) | GET |  |
| [Count Process Instance Tasks Due Today for Me](actions/count-process-instance-tasks-due-today-for-me.md) | GET |  |
| [Count Process Instance Tasks Due Today for User](actions/count-process-instance-tasks-due-today-for-user.md) | GET |  |
| [Count Process Instance Tasks for Process Template Task in Process Instance Header](actions/count-process-instance-tasks-for-process-template-task-in-process-instance-header.md) | GET |  |
| [Count Used Process Template Task Responses for Process Instance Header](actions/count-used-process-template-task-responses-for-process-instance-header.md) | GET |  |
| [Create Personal Task](actions/create-personal-task.md) | POST |  |
| [Create Process Instance Task for Process Instance Header](actions/create-process-instance-task-for-process-instance-header.md) | POST |  |
| [Delete Process Instance Task](actions/delete-process-instance-task.md) | DELETE |  |
| [Get Most Recently Completed Process Instance Task for Process Instance Header](actions/get-most-recently-completed-process-instance-task-for-process-instance-header.md) | GET |  |
| [Get Oldest Process Instance Task for Process Template Task](actions/get-oldest-process-instance-task-for-process-template-task.md) | GET |  |
| [Get Process Instance Task](actions/get-process-instance-task.md) | GET |  |
| [Get Process Instance Task Completed By User for Process Template Task](actions/get-process-instance-task-completed-by-user-for-process-template-task.md) | GET |  |
| [Get Process Instance Task for Process Template Task in Process Instance Header](actions/get-process-instance-task-for-process-template-task-in-process-instance-header.md) | GET |  |
| [Get Total Actual Time Today for Process Instance Tasks for Me](actions/get-total-actual-time-today-for-process-instance-tasks-for-me.md) | GET |  |
| [Get Total Actual Time Today for Process Instance Tasks for User](actions/get-total-actual-time-today-for-process-instance-tasks-for-user.md) | GET |  |
| [List Canceled Process Instance Tasks](actions/list-canceled-process-instance-tasks.md) | GET |  |
| [List Canceled Process Instance Tasks for Me](actions/list-canceled-process-instance-tasks-for-me.md) | GET |  |
| [List Canceled Process Instance Tasks for User](actions/list-canceled-process-instance-tasks-for-user.md) | GET |  |
| [List Completed Process Instance Tasks](actions/list-completed-process-instance-tasks.md) | GET |  |
| [List Completed Process Instance Tasks for Me](actions/list-completed-process-instance-tasks-for-me.md) | GET |  |
| [List Completed Process Instance Tasks for Process Instance Header](actions/list-completed-process-instance-tasks-for-process-instance-header.md) | GET |  |
| [List Completed Process Instance Tasks for Process Template Header](actions/list-completed-process-instance-tasks-for-process-template-header.md) | GET |  |
| [List Completed Process Instance Tasks for Process Template Task](actions/list-completed-process-instance-tasks-for-process-template-task.md) | GET |  |
| [List Completed Process Instance Tasks for User](actions/list-completed-process-instance-tasks-for-user.md) | GET |  |
| [List Past Due Process Instance Tasks](actions/list-past-due-process-instance-tasks.md) | GET |  |
| [List Past Due Process Instance Tasks for Me](actions/list-past-due-process-instance-tasks-for-me.md) | GET |  |
| [List Past Due Process Instance Tasks for User](actions/list-past-due-process-instance-tasks-for-user.md) | GET |  |
| [List Past Due Process Instance Tasks for User Group](actions/list-past-due-process-instance-tasks-for-user-group.md) | GET |  |
| [List Pending Process Instance Tasks](actions/list-pending-process-instance-tasks.md) | GET |  |
| [List Pending Process Instance Tasks for Me](actions/list-pending-process-instance-tasks-for-me.md) | GET |  |
| [List Pending Process Instance Tasks for Process Instance Header](actions/list-pending-process-instance-tasks-for-process-instance-header.md) | GET |  |
| [List Pending Process Instance Tasks for Process Template Task](actions/list-pending-process-instance-tasks-for-process-template-task.md) | GET |  |
| [List Pending Process Instance Tasks for User](actions/list-pending-process-instance-tasks-for-user.md) | GET |  |
| [List Pending Process Instance Tasks for User Group](actions/list-pending-process-instance-tasks-for-user-group.md) | GET |  |
| [List Process Instance Tasks](actions/list-process-instance-tasks.md) | GET |  |
| [List Process Instance Tasks Due Today](actions/list-process-instance-tasks-due-today.md) | GET |  |
| [List Process Instance Tasks Due Today for Me](actions/list-process-instance-tasks-due-today-for-me.md) | GET |  |
| [List Process Instance Tasks Due Today for User](actions/list-process-instance-tasks-due-today-for-user.md) | GET |  |
| [List Process Instance Tasks for Process Instance Header](actions/list-process-instance-tasks-for-process-instance-header.md) | GET |  |
| [List Process Instance Tasks for Process Template Task](actions/list-process-instance-tasks-for-process-template-task.md) | GET |  |
| [List Process Instance Tasks With Notes for Process Instance Header](actions/list-process-instance-tasks-with-notes-for-process-instance-header.md) | GET |  |
| [List Process Instance Tasks With Process Instance Fields for Process Template Header](actions/list-process-instance-tasks-with-process-instance-fields-for-process-template-header.md) | GET |  |
| [List Process Instance Tasks With Process Instance Fields for Process Template Task](actions/list-process-instance-tasks-with-process-instance-fields-for-process-template-task.md) | GET |  |
| [List Public Pending Process Instance Tasks for Process Instance Header](actions/list-public-pending-process-instance-tasks-for-process-instance-header.md) | GET |  |
| [Respond to Process Instance Task](actions/respond-to-process-instance-task.md) | POST |  |
| [Respond to Process Instance Tasks](actions/respond-to-process-instance-tasks.md) | POST |  |
| [Respond to Process Template Task for Process Instance Header](actions/respond-to-process-template-task-for-process-instance-header.md) | POST |  |
| [Start Process Template Task for Process Instance Header](actions/start-process-template-task-for-process-instance-header.md) | POST |  |
| [Update Process Instance Task](actions/update-process-instance-task.md) | PUT |  |
| [Update Process Instance Tasks](actions/update-process-instance-tasks.md) | PUT |  |

### Process Instance Task Checklist

| Action | Method | Description |
| --- | --- | --- |
| [Count Completed Process Instance Task Checklists for Process Instance Task](actions/count-completed-process-instance-task-checklists-for-process-instance-task.md) | GET |  |
| [Count Pending Process Instance Task Checklists for Process Instance Task](actions/count-pending-process-instance-task-checklists-for-process-instance-task.md) | GET |  |
| [Count Process Instance Task Checklists for Process Instance Task](actions/count-process-instance-task-checklists-for-process-instance-task.md) | GET |  |
| [Create Process Instance Task Checklist for Process Instance Task](actions/create-process-instance-task-checklist-for-process-instance-task.md) | POST |  |
| [Delete Process Instance Task Checklist](actions/delete-process-instance-task-checklist.md) | DELETE |  |
| [Get Process Instance Task Checklist](actions/get-process-instance-task-checklist.md) | GET |  |
| [List Completed Process Instance Task Checklists for Process Instance Task](actions/list-completed-process-instance-task-checklists-for-process-instance-task.md) | GET |  |
| [List Process Instance Task Checklists for Process Instance Task](actions/list-process-instance-task-checklists-for-process-instance-task.md) | GET |  |
| [List Process Instance Task Checklists for Process Template Task in Process Instance Header](actions/list-process-instance-task-checklists-for-process-template-task-in-process-instance-header.md) | GET |  |
| [Update Process Instance Task Checklist](actions/update-process-instance-task-checklist.md) | PUT |  |
| [Update Process Instance Task Checklists for Process Instance Task](actions/update-process-instance-task-checklists-for-process-instance-task.md) | PUT |  |

### Process Instance Task Tag

| Action | Method | Description |
| --- | --- | --- |
| [Apply Tag for Process Instance Task](actions/apply-tag-for-process-instance-task.md) | PUT |  |
| [Get Tag for Process Instance Task](actions/get-tag-for-process-instance-task.md) | GET |  |
| [List Process Instance Tasks for Tag](actions/list-process-instance-tasks-for-tag.md) | GET |  |
| [List Tags for Process Instance Task](actions/list-tags-for-process-instance-task.md) | GET |  |
| [Remove Tag for Process Instance Task](actions/remove-tag-for-process-instance-task.md) | DELETE |  |

### Process Template Connector

| Action | Method | Description |
| --- | --- | --- |
| [Create Process Template Connector for Process Template Header](actions/create-process-template-connector-for-process-template-header.md) | POST |  |
| [Delete Process Template Connector](actions/delete-process-template-connector.md) | DELETE |  |
| [Duplicate Process Template Connector into Process Template Header](actions/duplicate-process-template-connector-into-process-template-header.md) | POST |  |
| [Get Diagram Link for Creates in Process Template Connectors in Process Template Header](actions/get-diagram-link-for-creates-in-process-template-connectors-in-process-template-header.md) | POST |  |
| [Get Process Template Connector](actions/get-process-template-connector.md) | GET |  |
| [Get Process Template Connector for Process Template Header](actions/get-process-template-connector-for-process-template-header.md) | GET |  |
| [Update Process Template Connector](actions/update-process-template-connector.md) | PUT |  |

### Process Template Connector Field Mapping

| Action | Method | Description |
| --- | --- | --- |
| [Create All Field Mapping for Process Template Connectors in Process Template Connector](actions/create-all-field-mapping-for-process-template-connectors-in-process-template-connector.md) | POST |  |
| [Create Field Mapping for Process Template Connectors in Process Template Connector](actions/create-field-mapping-for-process-template-connectors-in-process-template-connector.md) | POST |  |
| [Delete Field Mapping for Process Template Connectors](actions/delete-field-mapping-for-process-template-connectors.md) | DELETE |  |
| [Get Field Mapping for Process Template Connectors](actions/get-field-mapping-for-process-template-connectors.md) | GET |  |
| [List Field Mappings for Process Template Connectors in Process Template Connector](actions/list-field-mappings-for-process-template-connectors-in-process-template-connector.md) | GET |  |
| [Update Field Mapping for Process Template Connectors](actions/update-field-mapping-for-process-template-connectors.md) | PUT |  |

### Process Template Field

| Action | Method | Description |
| --- | --- | --- |
| [Count Process Template Fields for Process Template Header](actions/count-process-template-fields-for-process-template-header.md) | GET |  |
| [Create Process Template Field for Message in Process Template Header](actions/create-process-template-field-for-message-in-process-template-header.md) | POST |  |
| [Create Process Template Field for Process Template Header](actions/create-process-template-field-for-process-template-header.md) | POST |  |
| [Delete Process Template Field](actions/delete-process-template-field.md) | DELETE |  |
| [Delete Process Template Fields for Process Template Header](actions/delete-process-template-fields-for-process-template-header.md) | DELETE |  |
| [Duplicate Process Template Field](actions/duplicate-process-template-field.md) | POST |  |
| [Get Custom Data Query Result As Text Value for Process Template Field](actions/get-custom-data-query-result-as-text-value-for-process-template-field.md) | GET |  |
| [Get Process Template Field](actions/get-process-template-field.md) | GET |  |
| [List Process Instance Fields For Bulk Edits for Process Template Header](actions/list-process-instance-fields-for-bulk-edits-for-process-template-header.md) | GET |  |
| [List Process Instance Fields for Process Template Header](actions/list-process-instance-fields-for-process-template-header.md) | GET |  |
| [List Process Instance Fields Start for Process Template Header](actions/list-process-instance-fields-start-for-process-template-header.md) | GET |  |
| [List Process Template Fields As Text Values for Process Template Header](actions/list-process-template-fields-as-text-values-for-process-template-header.md) | GET |  |
| [List Process Template Fields Date Fields Only for Process Template Header](actions/list-process-template-fields-date-fields-only-for-process-template-header.md) | GET |  |
| [List Process Template Fields File Attachment Fields Only for Process Template Header](actions/list-process-template-fields-file-attachment-fields-only-for-process-template-header.md) | GET |  |
| [List Process Template Fields for Process Template Field](actions/list-process-template-fields-for-process-template-field.md) | GET |  |
| [List Process Template Fields for Process Template Header](actions/list-process-template-fields-for-process-template-header.md) | GET |  |
| [List Process Template Fields For Table Views for Process Template Header](actions/list-process-template-fields-for-table-views-for-process-template-header.md) | GET |  |
| [List Process Template Fields Instance Reference Fields Only for Process Template Header](actions/list-process-template-fields-instance-reference-fields-only-for-process-template-header.md) | GET |  |
| [List Process Template Fields Process Table Discrete Fields Only for Process Template Header](actions/list-process-template-fields-process-table-discrete-fields-only-for-process-template-header.md) | GET |  |
| [List Process Template Fields User Fields Only for Process Template Header](actions/list-process-template-fields-user-fields-only-for-process-template-header.md) | GET |  |
| [Update Process Template Field](actions/update-process-template-field.md) | PUT |  |
| [Update Process Template Fields for Process Template Header](actions/update-process-template-fields-for-process-template-header.md) | PUT |  |

### Process Template Field File

| Action | Method | Description |
| --- | --- | --- |
| [Apply File for Process Template Task](actions/apply-file-for-process-template-task.md) | PUT |  |
| [Create File for Process Template Field](actions/create-file-for-process-template-field.md) | POST |  |
| [Create File for Process Template Header](actions/create-file-for-process-template-header.md) | POST |  |
| [Create File for Process Template Task](actions/create-file-for-process-template-task.md) | POST |  |
| [Get File for Process Template Field](actions/get-file-for-process-template-field.md) | GET |  |
| [Get File for Process Template Header](actions/get-file-for-process-template-header.md) | GET |  |
| [Get File for Process Template Task](actions/get-file-for-process-template-task.md) | GET |  |
| [List Files for Process Instance Task](actions/list-files-for-process-instance-task.md) | GET |  |
| [List Files for Process Template Field](actions/list-files-for-process-template-field.md) | GET |  |
| [List Files for Process Template Header](actions/list-files-for-process-template-header.md) | GET |  |
| [List Files for Process Template Headers](actions/list-files-for-process-template-headers.md) | GET |  |
| [List Files for Process Template Task](actions/list-files-for-process-template-task.md) | GET |  |
| [Remove File for Process Template Field](actions/remove-file-for-process-template-field.md) | DELETE |  |
| [Remove File for Process Template Header](actions/remove-file-for-process-template-header.md) | DELETE |  |
| [Remove File for Process Template Task](actions/remove-file-for-process-template-task.md) | DELETE |  |
| [Update File for Process Template Header](actions/update-file-for-process-template-header.md) | PUT |  |
| [Update File for Process Template Task](actions/update-file-for-process-template-task.md) | PUT |  |

### Process Template Field Option

| Action | Method | Description |
| --- | --- | --- |
| [Count Process Template Field Options for Process Template Field](actions/count-process-template-field-options-for-process-template-field.md) | GET |  |
| [Create Process Template Field Option for Process Template Field](actions/create-process-template-field-option-for-process-template-field.md) | POST |  |
| [Delete Process Template Field Option](actions/delete-process-template-field-option.md) | DELETE |  |
| [Delete Process Template Field Options for Process Template Field](actions/delete-process-template-field-options-for-process-template-field.md) | DELETE |  |
| [Get Process Template Field Option](actions/get-process-template-field-option.md) | GET |  |
| [List Process Template Field Options for Process Template Field](actions/list-process-template-field-options-for-process-template-field.md) | GET |  |
| [List Process Template Field Options for Process Template Header](actions/list-process-template-field-options-for-process-template-header.md) | GET |  |
| [Update Process Template Field Option](actions/update-process-template-field-option.md) | PUT |  |
| [Update Process Template Field Options for Process Template Field](actions/update-process-template-field-options-for-process-template-field.md) | PUT |  |

### Process Template Group

| Action | Method | Description |
| --- | --- | --- |
| [Convert Process Template Groups IDs to Objects](actions/convert-process-template-groups-i-ds-to-objects.md) | GET |  |
| [Count Process Template Groups](actions/count-process-template-groups.md) | GET |  |
| [Create Process Template Group](actions/create-process-template-group.md) | POST |  |
| [Delete Process Template Group](actions/delete-process-template-group.md) | DELETE |  |
| [Delete Process Template Groups](actions/delete-process-template-groups.md) | DELETE |  |
| [Get Process Template Group](actions/get-process-template-group.md) | GET |  |
| [List Process Template Groups](actions/list-process-template-groups.md) | GET |  |
| [Update Process Template Group](actions/update-process-template-group.md) | PUT |  |

### Process Template Header

| Action | Method | Description |
| --- | --- | --- |
| [Convert Process Template Headers IDs to Objects](actions/convert-process-template-headers-i-ds-to-objects.md) | GET |  |
| [Copy Process Template Header](actions/copy-process-template-header.md) | POST |  |
| [Count Process Template Headers](actions/count-process-template-headers.md) | GET |  |
| [Count Process Template Headers With Process Instance Header Pending](actions/count-process-template-headers-with-process-instance-header-pending.md) | GET |  |
| [Create Process Template Header](actions/create-process-template-header.md) | POST |  |
| [Delete Process Template Header](actions/delete-process-template-header.md) | DELETE |  |
| [Delete Process Template Headers](actions/delete-process-template-headers.md) | DELETE |  |
| [Export JSON for Process Template Header](actions/export-json-for-process-template-header.md) | GET |  |
| [Get Diagram Builder for AI Agents in Process Template Header](actions/get-diagram-builder-for-ai-agents-in-process-template-header.md) | POST |  |
| [Get Diagram for Defaults in Creates in Process Template Headers](actions/get-diagram-for-defaults-in-creates-in-process-template-headers.md) | POST |  |
| [Get Process Template Header](actions/get-process-template-header.md) | GET |  |
| [Get Process Template Header Import Knowledge Examples](actions/get-process-template-header-import-knowledge-examples.md) | POST |  |
| [Get Scheduled AI Prompt for Creates in Process Template Headers](actions/get-scheduled-ai-prompt-for-creates-in-process-template-headers.md) | POST |  |
| [Get Store Import for Process Template Header in Process Template Category](actions/get-store-import-for-process-template-header-in-process-template-category.md) | GET |  |
| [Get Store Preview for Process Template Header in Process Template Category](actions/get-store-preview-for-process-template-header-in-process-template-category.md) | GET |  |
| [Import JSON File for Process Template Header](actions/import-json-file-for-process-template-header.md) | POST |  |
| [List Field Tokens for Independents in Process Template Headers](actions/list-field-tokens-for-independents-in-process-template-headers.md) | GET |  |
| [List Field Tokens for Process Template Header](actions/list-field-tokens-for-process-template-header.md) | GET |  |
| [List Process Template Headers](actions/list-process-template-headers.md) | GET |  |
| [List Process Template Headers As Text Values](actions/list-process-template-headers-as-text-values.md) | GET |  |
| [List Process Template Headers for Process Template Group](actions/list-process-template-headers-for-process-template-group.md) | GET |  |
| [List Process Template Headers for Proxy Job](actions/list-process-template-headers-for-proxy-job.md) | GET |  |
| [List Process Template Headers For Starting](actions/list-process-template-headers-for-starting.md) | GET |  |
| [List Process Template Headers With Primary Document](actions/list-process-template-headers-with-primary-document.md) | GET |  |
| [List Process Template Headers With Primary Document As Text Values](actions/list-process-template-headers-with-primary-document-as-text-values.md) | GET |  |
| [List Process Template Headers With Primary Document For Starting](actions/list-process-template-headers-with-primary-document-for-starting.md) | GET |  |
| [List Stores for Process Template Headers in Process Template Category](actions/list-stores-for-process-template-headers-in-process-template-category.md) | GET |  |
| [List Work Schedules for Field Tokens in Process Template Header](actions/list-work-schedules-for-field-tokens-in-process-template-header.md) | GET |  |
| [Start Process Template Header](actions/start-process-template-header.md) | POST |  |
| [Store Purchase for Process Template Header for Process Template Category](actions/store-purchase-for-process-template-header-for-process-template-category.md) | POST |  |
| [Update Process Template Header](actions/update-process-template-header.md) | PUT |  |

### Process Template Public Form

| Action | Method | Description |
| --- | --- | --- |
| [Count Process Template Public Forms](actions/count-process-template-public-forms.md) | GET |  |
| [Create Process Template Public Form for Process Template Header](actions/create-process-template-public-form-for-process-template-header.md) | POST |  |
| [Delete Logo for Process Template Public Form](actions/delete-logo-for-process-template-public-form.md) | DELETE |  |
| [Delete Process Template Public Form](actions/delete-process-template-public-form.md) | DELETE |  |
| [Get Process Template Public Form](actions/get-process-template-public-form.md) | GET |  |
| [Get Success Status for Process Instance Header in Process Template Public Form](actions/get-success-status-for-process-instance-header-in-process-template-public-form.md) | GET |  |
| [List Process Instance Fields for Process Template Public Form](actions/list-process-instance-fields-for-process-template-public-form.md) | GET |  |
| [List Process Template Public Forms for Process Template Header](actions/list-process-template-public-forms-for-process-template-header.md) | GET |  |
| [Start Process Instance Header for Process Template Public Form](actions/start-process-instance-header-for-process-template-public-form.md) | POST |  |
| [Update Logo for Process Template Public Form](actions/update-logo-for-process-template-public-form.md) | PUT |  |
| [Update Process Instance Fields for Process Template Public Form](actions/update-process-instance-fields-for-process-template-public-form.md) | PUT |  |
| [Update Process Template Public Form](actions/update-process-template-public-form.md) | PUT |  |

### Process Template Task

| Action | Method | Description |
| --- | --- | --- |
| [Convert Process Template Tasks IDs to Objects](actions/convert-process-template-tasks-i-ds-to-objects.md) | GET |  |
| [Count Unique Process Template Tasks for Process Template Header](actions/count-unique-process-template-tasks-for-process-template-header.md) | GET |  |
| [Create Process Template Task for Process Template Header](actions/create-process-template-task-for-process-template-header.md) | POST |  |
| [Delete Process Template Task](actions/delete-process-template-task.md) | DELETE |  |
| [Duplicate Process Template Task into Process Template Header](actions/duplicate-process-template-task-into-process-template-header.md) | POST |  |
| [Get AI Agent Job for Process Template Task](actions/get-ai-agent-job-for-process-template-task.md) | GET |  |
| [Get Process Template Task](actions/get-process-template-task.md) | GET |  |
| [List Process Template Fields for Process Template Task](actions/list-process-template-fields-for-process-template-task.md) | GET |  |
| [List Process Template Tasks](actions/list-process-template-tasks.md) | GET |  |
| [List Process Template Tasks As Text Values for Process Template Header](actions/list-process-template-tasks-as-text-values-for-process-template-header.md) | GET |  |
| [List Process Template Tasks for Process Template Header](actions/list-process-template-tasks-for-process-template-header.md) | GET |  |
| [List Process Template Tasks for User](actions/list-process-template-tasks-for-user.md) | GET |  |
| [Update Process Template Task](actions/update-process-template-task.md) | PUT |  |
| [Update Process Template Tasks](actions/update-process-template-tasks.md) | PUT |  |

### Process Template Task Checklist

| Action | Method | Description |
| --- | --- | --- |
| [Create Process Template Task Checklist for Process Template Task](actions/create-process-template-task-checklist-for-process-template-task.md) | POST |  |
| [Delete Process Template Task Checklist](actions/delete-process-template-task-checklist.md) | DELETE |  |
| [Delete Process Template Task Checklists for Process Template Task](actions/delete-process-template-task-checklists-for-process-template-task.md) | DELETE |  |
| [Get Process Template Task Checklist](actions/get-process-template-task-checklist.md) | GET |  |
| [List Process Template Task Checklists for Process Template Header](actions/list-process-template-task-checklists-for-process-template-header.md) | GET |  |
| [List Process Template Task Checklists for Process Template Task](actions/list-process-template-task-checklists-for-process-template-task.md) | GET |  |
| [Update Process Template Task Checklist](actions/update-process-template-task-checklist.md) | PUT |  |
| [Update Process Template Task Checklists for Process Template Task](actions/update-process-template-task-checklists-for-process-template-task.md) | PUT |  |

### Process Template Task Response

| Action | Method | Description |
| --- | --- | --- |
| [Count Unique Process Template Task Responses for Process Template Header](actions/count-unique-process-template-task-responses-for-process-template-header.md) | GET |  |
| [Create Process Template Task Response for Process Template Header](actions/create-process-template-task-response-for-process-template-header.md) | POST |  |
| [Delete Process Template Task Response](actions/delete-process-template-task-response.md) | DELETE |  |
| [Duplicate Process Template Task Response into Process Template Header](actions/duplicate-process-template-task-response-into-process-template-header.md) | POST |  |
| [Get Process Template Task Response](actions/get-process-template-task-response.md) | GET |  |
| [List Non Neutral Process Template Task Responses](actions/list-non-neutral-process-template-task-responses.md) | GET |  |
| [List Unique Non Neutral Process Template Task Responses for Process Template Header](actions/list-unique-non-neutral-process-template-task-responses-for-process-template-header.md) | GET |  |
| [List Unique Process Template Task Responses for Process Template Header](actions/list-unique-process-template-task-responses-for-process-template-header.md) | GET |  |
| [Update Process Template Task Response](actions/update-process-template-task-response.md) | PUT |  |

### Process Template Task Tag Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Apply Tag for Process Template Task](actions/apply-tag-for-process-template-task.md) | PUT |  |
| [Get Tag for Process Template Task](actions/get-tag-for-process-template-task.md) | GET |  |
| [List Process Template Tasks for Tag](actions/list-process-template-tasks-for-tag.md) | GET |  |
| [List Tags for Process Template Task](actions/list-tags-for-process-template-task.md) | GET |  |
| [Remove Tag for Process Template Task](actions/remove-tag-for-process-template-task.md) | DELETE |  |

### Process Template Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Process Template Webhook for Process Template Header](actions/create-process-template-webhook-for-process-template-header.md) | POST |  |
| [Delete Process Template Webhook](actions/delete-process-template-webhook.md) | DELETE |  |
| [Get Process Template Webhook](actions/get-process-template-webhook.md) | GET |  |
| [List Process Template Webhooks for Process Template Header](actions/list-process-template-webhooks-for-process-template-header.md) | GET |  |
| [Start Process Instance Header for Process Template Webhook](actions/start-process-instance-header-for-process-template-webhook.md) | POST |  |
| [Update Process Template Webhook](actions/update-process-template-webhook.md) | PUT |  |

### Process Template Webhook Field Mapping

| Action | Method | Description |
| --- | --- | --- |
| [Create Field Mapping for Process Template Webhooks in Process Template Webhook](actions/create-field-mapping-for-process-template-webhooks-in-process-template-webhook.md) | POST |  |
| [Delete Field Mapping for Process Template Webhooks](actions/delete-field-mapping-for-process-template-webhooks.md) | DELETE |  |
| [Get Field Mapping for Process Template Webhooks](actions/get-field-mapping-for-process-template-webhooks.md) | GET |  |
| [Get Field Mapping for Process Template Webhooks in Process Template Field in Process Template Webhook](actions/get-field-mapping-for-process-template-webhooks-in-process-template-field-in-process-template-webhook.md) | GET |  |
| [List Field Mappings for Process Template Webhooks in Process Template Webhook](actions/list-field-mappings-for-process-template-webhooks-in-process-template-webhook.md) | GET |  |
| [Search Field Mappings for Process Template Webhooks in Process Template Webhook](actions/search-field-mappings-for-process-template-webhooks-in-process-template-webhook.md) | GET |  |
| [Update Field Mapping for Process Template Webhooks](actions/update-field-mapping-for-process-template-webhooks.md) | PUT |  |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Count Process Instance Task Report Series Past Due Grouped By Process Template Task for Process Template Header](actions/count-process-instance-task-report-series-past-due-grouped-by-process-template-task-for-process-template-header.md) | GET |  |
| [Count Process Instance Task Report Series Past Due Grouped By User for Process Template Header](actions/count-process-instance-task-report-series-past-due-grouped-by-user-for-process-template-header.md) | GET |  |
| [Count Process Instance Task Report Series Past Due Grouped By User for Process Template Task](actions/count-process-instance-task-report-series-past-due-grouped-by-user-for-process-template-task.md) | GET |  |
| [Count Process Instance Task Report Series Pending Grouped By Process Template Task for Process Template Header](actions/count-process-instance-task-report-series-pending-grouped-by-process-template-task-for-process-template-header.md) | GET |  |
| [Count Process Instance Task Report Series Pending Grouped By User for Process Template Header](actions/count-process-instance-task-report-series-pending-grouped-by-user-for-process-template-header.md) | GET |  |
| [Count Process Instance Task Report Series Pending Grouped By User for Process Template Task](actions/count-process-instance-task-report-series-pending-grouped-by-user-for-process-template-task.md) | GET |  |
| [List Process Instance Header Report Series Created Grouped By Day for Process Template Header](actions/list-process-instance-header-report-series-created-grouped-by-day-for-process-template-header.md) | GET |  |
| [List Process Instance Header Report Series Grouped By Assigned To Full Name](actions/list-process-instance-header-report-series-grouped-by-assigned-to-full-name.md) | GET |  |
| [List Process Instance Header Report Series Grouped By Completed Day](actions/list-process-instance-header-report-series-grouped-by-completed-day.md) | GET |  |
| [List Process Instance Header Report Series Grouped By Completed Month](actions/list-process-instance-header-report-series-grouped-by-completed-month.md) | GET |  |
| [List Process Instance Header Report Series Grouped By Instance Age Minutes](actions/list-process-instance-header-report-series-grouped-by-instance-age-minutes.md) | GET |  |
| [List Process Instance Header Report Series Grouped By Instance Average Completion Minutes](actions/list-process-instance-header-report-series-grouped-by-instance-average-completion-minutes.md) | GET |  |
| [List Process Instance Header Report Series Grouped By Pending Task Name](actions/list-process-instance-header-report-series-grouped-by-pending-task-name.md) | GET |  |
| [List Process Instance Header Report Series Grouped By Process Template Field Value](actions/list-process-instance-header-report-series-grouped-by-process-template-field-value.md) | GET |  |
| [List Process Instance Header Report Series Grouped By Started Day](actions/list-process-instance-header-report-series-grouped-by-started-day.md) | GET |  |
| [List Process Instance Header Report Series Grouped By Started Month](actions/list-process-instance-header-report-series-grouped-by-started-month.md) | GET |  |
| [List Process Instance Header Report Series Past Due Grouped By Process Template Header](actions/list-process-instance-header-report-series-past-due-grouped-by-process-template-header.md) | GET |  |
| [List Process Instance Header Report Series Past Due Grouped By Process Template Header for User Group](actions/list-process-instance-header-report-series-past-due-grouped-by-process-template-header-for-user-group.md) | GET |  |
| [List Process Instance Header Report Series Past Due Grouped By User for Process Template Group](actions/list-process-instance-header-report-series-past-due-grouped-by-user-for-process-template-group.md) | GET |  |
| [List Process Instance Header Report Series Past Due Grouped By User for Process Template Header](actions/list-process-instance-header-report-series-past-due-grouped-by-user-for-process-template-header.md) | GET |  |
| [List Process Instance Header Report Series Pending Grouped By Process Template Header](actions/list-process-instance-header-report-series-pending-grouped-by-process-template-header.md) | GET |  |
| [List Process Instance Header Report Series Pending Grouped By Process Template Header for User Group](actions/list-process-instance-header-report-series-pending-grouped-by-process-template-header-for-user-group.md) | GET |  |
| [List Process Instance Header Report Series Pending Grouped By User for Process Template Group](actions/list-process-instance-header-report-series-pending-grouped-by-user-for-process-template-group.md) | GET |  |
| [List Process Instance Header Report Series Pending Grouped By User for Process Template Header](actions/list-process-instance-header-report-series-pending-grouped-by-user-for-process-template-header.md) | GET |  |
| [List Process Instance Task Report Series Average Age Grouped By Process Template Task for Process Template Header](actions/list-process-instance-task-report-series-average-age-grouped-by-process-template-task-for-process-template-header.md) | GET |  |
| [List Process Instance Task Report Series Average Age Grouped By User for Process Template Task](actions/list-process-instance-task-report-series-average-age-grouped-by-user-for-process-template-task.md) | GET |  |
| [List Process Instance Task Report Series Average Duration Grouped By Process Template Task for Process Template Header](actions/list-process-instance-task-report-series-average-duration-grouped-by-process-template-task-for-process-template-header.md) | GET |  |
| [List Process Instance Task Report Series Average Duration Grouped By User for Process Template Task](actions/list-process-instance-task-report-series-average-duration-grouped-by-user-for-process-template-task.md) | GET |  |
| [List Process Instance Task Report Series Average Duration Grouped By User for User Group](actions/list-process-instance-task-report-series-average-duration-grouped-by-user-for-user-group.md) | GET |  |
| [List Process Instance Task Report Series Backlog Time Grouped By User for User Group](actions/list-process-instance-task-report-series-backlog-time-grouped-by-user-for-user-group.md) | GET |  |
| [List Process Instance Task Report Series Grouped By Assigned To Full Name](actions/list-process-instance-task-report-series-grouped-by-assigned-to-full-name.md) | GET |  |
| [List Process Instance Task Report Series Grouped By Canceled By Full Name](actions/list-process-instance-task-report-series-grouped-by-canceled-by-full-name.md) | GET |  |
| [List Process Instance Task Report Series Grouped By Completed By Full Name](actions/list-process-instance-task-report-series-grouped-by-completed-by-full-name.md) | GET |  |
| [List Process Instance Task Report Series Grouped By Completed Day](actions/list-process-instance-task-report-series-grouped-by-completed-day.md) | GET |  |
| [List Process Instance Task Report Series Grouped By Completed Month](actions/list-process-instance-task-report-series-grouped-by-completed-month.md) | GET |  |
| [List Process Instance Task Report Series Grouped By Process Template Response Name](actions/list-process-instance-task-report-series-grouped-by-process-template-response-name.md) | GET |  |
| [List Process Instance Task Report Series Grouped By Process Template Task Name](actions/list-process-instance-task-report-series-grouped-by-process-template-task-name.md) | GET |  |
| [List Process Instance Task Report Series Grouped By Task Average Completion Minutes](actions/list-process-instance-task-report-series-grouped-by-task-average-completion-minutes.md) | GET |  |
| [List Process Instance Task Report Series Grouped By User Average Completion Minutes](actions/list-process-instance-task-report-series-grouped-by-user-average-completion-minutes.md) | GET |  |
| [List Process Instance Task Report Series Grouped By User Average Pending Age Minutes](actions/list-process-instance-task-report-series-grouped-by-user-average-pending-age-minutes.md) | GET |  |
| [List Process Instance Task Report Series Max Age Grouped By Process Template Task for Process Template Header](actions/list-process-instance-task-report-series-max-age-grouped-by-process-template-task-for-process-template-header.md) | GET |  |
| [List Process Instance Task Report Series Max Age Grouped By User for Process Template Task](actions/list-process-instance-task-report-series-max-age-grouped-by-user-for-process-template-task.md) | GET |  |
| [List Process Instance Task Report Series Past Due Grouped By User for User Group](actions/list-process-instance-task-report-series-past-due-grouped-by-user-for-user-group.md) | GET |  |
| [List Process Instance Task Report Series Pending Grouped By User for User Group](actions/list-process-instance-task-report-series-pending-grouped-by-user-for-user-group.md) | GET |  |
| [List Process Template Task Response Report Series Percent Grouped By Process Template Task Response for Process Template Task](actions/list-process-template-task-response-report-series-percent-grouped-by-process-template-task-response-for-process-template-task.md) | GET |  |
| [List Today Report Series Grouped By Process Instance Header for User](actions/list-today-report-series-grouped-by-process-instance-header-for-user.md) | GET |  |
| [List Today Report Series Grouped By User for Process Instance Header](actions/list-today-report-series-grouped-by-user-for-process-instance-header.md) | GET |  |
| [List Weekly Time Report Series Grouped By Process Instance Header for User](actions/list-weekly-time-report-series-grouped-by-process-instance-header-for-user.md) | GET |  |
| [List Weekly Time Report Series Grouped By User for Process Instance Header](actions/list-weekly-time-report-series-grouped-by-user-for-process-instance-header.md) | GET |  |

### Session Token

| Action | Method | Description |
| --- | --- | --- |
| [Create API Token for Me](actions/create-api-token-for-me.md) | POST |  |
| [Create API Token for Proxy](actions/create-api-token-for-proxy.md) | POST |  |
| [Create Mobile App Token for Me in Private Users](actions/create-mobile-app-token-for-me-in-private-users.md) | POST |  |
| [Create Private File Access Token for Me in Private Users](actions/create-private-file-access-token-for-me-in-private-users.md) | POST |  |
| [Create Public Table Token for Process Template Header](actions/create-public-table-token-for-process-template-header.md) | POST |  |
| [Create Start Email for Process Template Header](actions/create-start-email-for-process-template-header.md) | POST |  |
| [Delete API Token for Me](actions/delete-api-token-for-me.md) | DELETE |  |
| [Delete API Token for Proxy](actions/delete-api-token-for-proxy.md) | DELETE |  |
| [Delete Public Table Token for Process Template Header](actions/delete-public-table-token-for-process-template-header.md) | DELETE |  |
| [Delete Start Email for Process Template Header](actions/delete-start-email-for-process-template-header.md) | DELETE |  |
| [Get One Time App Linkup Code](actions/get-one-time-app-linkup-code.md) | POST |  |
| [Get Public Milestone Access Token for Process Instance Header](actions/get-public-milestone-access-token-for-process-instance-header.md) | GET |  |
| [List API Tokens for Me](actions/list-api-tokens-for-me.md) | GET |  |
| [List API Tokens for Proxy](actions/list-api-tokens-for-proxy.md) | GET |  |
| [List Public Table Tokens for Process Template Header](actions/list-public-table-tokens-for-process-template-header.md) | GET |  |
| [List Start Emails for Process Template Header](actions/list-start-emails-for-process-template-header.md) | GET |  |

### Sms

| Action | Method | Description |
| --- | --- | --- |
| [Count SMS](actions/count-sms.md) | GET |  |
| [Get SMS](actions/get-sms.md) | GET |  |
| [List SMS](actions/list-sms.md) | GET |  |

### Standard Operation Procedure Template

| Action | Method | Description |
| --- | --- | --- |
| [Convert Standard Operation Procedure Templates IDs to Objects](actions/convert-standard-operation-procedure-templates-i-ds-to-objects.md) | GET |  |
| [Create Standard Operation Procedure Template](actions/create-standard-operation-procedure-template.md) | POST |  |
| [Delete Standard Operation Procedure Template](actions/delete-standard-operation-procedure-template.md) | DELETE |  |
| [Delete Standard Operation Procedure Templates](actions/delete-standard-operation-procedure-templates.md) | DELETE |  |
| [Get Process Template Header for Applies in Standard Operation Procedure Template](actions/get-process-template-header-for-applies-in-standard-operation-procedure-template.md) | GET |  |
| [Get Standard Operation Procedure Template](actions/get-standard-operation-procedure-template.md) | GET |  |
| [List Standard Operation Procedure Templates](actions/list-standard-operation-procedure-templates.md) | GET |  |
| [Update Standard Operation Procedure Template](actions/update-standard-operation-procedure-template.md) | PUT |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Convert Tags IDs to Objects](actions/convert-tags-i-ds-to-objects.md) | GET |  |
| [Count Tags](actions/count-tags.md) | GET |  |
| [Create Tag](actions/create-tag.md) | POST |  |
| [Delete Tag](actions/delete-tag.md) | DELETE |  |
| [Delete Tags](actions/delete-tags.md) | DELETE |  |
| [Get Tag](actions/get-tag.md) | GET |  |
| [List Tags](actions/list-tags.md) | GET |  |
| [Update Tag](actions/update-tag.md) | PUT |  |

### Text Block

| Action | Method | Description |
| --- | --- | --- |
| [Convert Text Blocks IDs to Objects](actions/convert-text-blocks-i-ds-to-objects.md) | GET |  |
| [Create Text Block](actions/create-text-block.md) | POST |  |
| [Delete Text Block](actions/delete-text-block.md) | DELETE |  |
| [Delete Text Blocks](actions/delete-text-blocks.md) | DELETE |  |
| [Get Text Block](actions/get-text-block.md) | GET |  |
| [List Text Blocks](actions/list-text-blocks.md) | GET |  |
| [Update Text Block](actions/update-text-block.md) | PUT |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Convert Users IDs to Objects](actions/convert-users-i-ds-to-objects.md) | GET |  |
| [Count Users](actions/count-users.md) | GET |  |
| [Create User](actions/create-user.md) | POST |  |
| [Delete Profile Picture for User](actions/delete-profile-picture-for-user.md) | DELETE |  |
| [Delete User](actions/delete-user.md) | DELETE |  |
| [Delete Users](actions/delete-users.md) | DELETE |  |
| [Get UI Context for Me](actions/get-ui-context-for-me.md) | GET |  |
| [Get User](actions/get-user.md) | GET |  |
| [Get User Me](actions/get-user-me.md) | GET |  |
| [Initiate Password Change for User](actions/initiate-password-change-for-user.md) | POST |  |
| [List Users](actions/list-users.md) | GET |  |
| [List Users As Text Values](actions/list-users-as-text-values.md) | GET |  |
| [Update Profile Picture for User](actions/update-profile-picture-for-user.md) | PUT |  |
| [Update User](actions/update-user.md) | PUT |  |

### User Custom Field Value

| Action | Method | Description |
| --- | --- | --- |
| [Count User Custom Field Values for User](actions/count-user-custom-field-values-for-user.md) | GET |  |
| [Create User Custom Field Value for User](actions/create-user-custom-field-value-for-user.md) | POST |  |
| [Delete User Custom Field Value](actions/delete-user-custom-field-value.md) | DELETE |  |
| [Get User Custom Field Value](actions/get-user-custom-field-value.md) | GET |  |
| [Get User Custom Field Value for User Custom Field in User](actions/get-user-custom-field-value-for-user-custom-field-in-user.md) | GET |  |
| [List User Custom Field Values for User](actions/list-user-custom-field-values-for-user.md) | GET |  |
| [List User Custom Field Values for User Custom Field](actions/list-user-custom-field-values-for-user-custom-field.md) | GET |  |
| [Refresh User Custom Field Values for User](actions/refresh-user-custom-field-values-for-user.md) | PUT |  |
| [Search User Custom Field Values for User](actions/search-user-custom-field-values-for-user.md) | GET |  |
| [Update User Custom Field Value](actions/update-user-custom-field-value.md) | PUT |  |

### User Customer Field

| Action | Method | Description |
| --- | --- | --- |
| [Count User Custom Fields](actions/count-user-custom-fields.md) | GET |  |
| [Create User Custom Field](actions/create-user-custom-field.md) | POST |  |
| [Delete User Custom Field](actions/delete-user-custom-field.md) | DELETE |  |
| [Delete User Custom Fields](actions/delete-user-custom-fields.md) | DELETE |  |
| [Get User Custom Field](actions/get-user-custom-field.md) | GET |  |
| [List User Custom Fields](actions/list-user-custom-fields.md) | GET |  |
| [Update User Custom Field](actions/update-user-custom-field.md) | PUT |  |
| [Update User Custom Fields](actions/update-user-custom-fields.md) | PUT |  |

### User Favorite

| Action | Method | Description |
| --- | --- | --- |
| [Create User Favorite for Me](actions/create-user-favorite-for-me.md) | POST |  |
| [Delete User Favorite for Me](actions/delete-user-favorite-for-me.md) | DELETE |  |
| [Get User Favorite for Me](actions/get-user-favorite-for-me.md) | GET |  |
| [List User Favorites for Me](actions/list-user-favorites-for-me.md) | GET |  |
| [Update User Favorite for Me](actions/update-user-favorite-for-me.md) | PUT |  |
| [Update User Favorites for Me](actions/update-user-favorites-for-me.md) | PUT |  |

### User Group

| Action | Method | Description |
| --- | --- | --- |
| [Convert User Groups IDs to Objects](actions/convert-user-groups-i-ds-to-objects.md) | GET |  |
| [Count User Groups](actions/count-user-groups.md) | GET |  |
| [Create User Group](actions/create-user-group.md) | POST |  |
| [Delete User Group](actions/delete-user-group.md) | DELETE |  |
| [Delete User Groups](actions/delete-user-groups.md) | DELETE |  |
| [Get User Group](actions/get-user-group.md) | GET |  |
| [List User Groups](actions/list-user-groups.md) | GET |  |
| [List User Groups As Text Values](actions/list-user-groups-as-text-values.md) | GET |  |
| [Update User Group](actions/update-user-group.md) | PUT |  |

### User Group Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Count Users for User Group](actions/count-users-for-user-group.md) | GET |  |
| [Get Add User for User Group](actions/get-add-user-for-user-group.md) | POST |  |
| [Get Add User Group for User](actions/get-add-user-group-for-user.md) | POST |  |
| [Get Remove User for User Group](actions/get-remove-user-for-user-group.md) | POST |  |
| [Get Remove User Group for User](actions/get-remove-user-group-for-user.md) | POST |  |
| [Get User for User Group](actions/get-user-for-user-group.md) | GET |  |
| [List User Group Users As Text Values](actions/list-user-group-users-as-text-values.md) | GET |  |
| [List User Groups for User](actions/list-user-groups-for-user.md) | GET |  |
| [List Users for User Group](actions/list-users-for-user-group.md) | GET |  |

### Work Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Count Work Schedules](actions/count-work-schedules.md) | GET |  |
| [Create Work Schedule](actions/create-work-schedule.md) | POST |  |
| [Delete Work Schedule](actions/delete-work-schedule.md) | DELETE |  |
| [Delete Work Schedules](actions/delete-work-schedules.md) | DELETE |  |
| [Get Work Schedule](actions/get-work-schedule.md) | GET |  |
| [List Work Schedules](actions/list-work-schedules.md) | GET |  |
| [Update Work Schedule](actions/update-work-schedule.md) | PUT |  |

