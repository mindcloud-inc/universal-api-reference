# <img src="https://images.mindcloud.co/apps/icons/couchbase-capella-icon_1776434460122.png" alt="Couchbase Capella logo" width="28" height="28"> Couchbase Capella: Universal API

Use the Couchbase Capella Management API to create and manage organizations, projects, clusters, buckets, App Services, backups, users, API keys, and related Capella resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/couchbaseCapella/latest
- **Category:** IT Operations / Database
- **Actions:** 259
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.couchbase.com/products/capella
- **Vendor API docs:** https://docs.couchbase.com/cloud/management-api-guide/management-api-intro.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organizations](actions/list-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/couchbaseCapella/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (259)

### Ai Services Providers

| Action | Method | Description |
| --- | --- | --- |
| [Create provider](actions/create-provider.md) | POST | Creates a provider in Couchbase Capella. |
| [Delete provider](actions/delete-provider.md) | DELETE | Deletes a provider from Couchbase Capella. |
| [Get provider](actions/get-provider.md) | GET | Retrieves a provider from Couchbase Capella. |
| [List providers](actions/list-providers.md) | GET | Retrieves providers from Couchbase Capella. |
| [Update provider](actions/update-provider.md) | PUT | Updates a provider in Couchbase Capella. |

### Ai Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Create AI Workflow](actions/create-ai-workflow.md) | POST | Creates an AI workflow in Couchbase Capella. |
| [Run an AI Workflow](actions/create-ai-workflow-run.md) | POST | Runs an AI workflow in Couchbase Capella. |
| [Delete AI Workflow](actions/delete-ai-workflow.md) | DELETE | Deletes an AI workflow from Couchbase Capella. |
| [Get AI Workflow](actions/get-ai-workflow.md) | GET | Retrieves an AI workflow from Couchbase Capella. |
| [Get AI Workflow Run](actions/get-ai-workflow-run.md) | GET | Retrieves an AI workflow run from Couchbase Capella. |
| [Get AI Workflow Run Processed Files](actions/get-ai-workflow-run-processed-files.md) | GET | Retrieves an AI workflow run processed files from Couchbase Capella. |
| [List AI Workflow Runs](actions/list-ai-workflow-runs.md) | GET | Retrieves AI workflow runs from Couchbase Capella. |
| [List AI Workflows](actions/list-ai-workflows.md) | GET | Retrieves AI workflows from Couchbase Capella. |
| [Stop AI Workflow Run](actions/stop-ai-workflow-run.md) | DELETE | Stops an AI workflow run in Couchbase Capella. |

### Alert Integration

| Action | Method | Description |
| --- | --- | --- |
| [Delete Alert Integration](actions/delete-alert-integration-by-id.md) | DELETE | Deletes an alert integration from Couchbase Capella. |
| [Get Alert Integration](actions/get-alert-integration-by-id.md) | GET | Retrieves an alert integration from Couchbase Capella. |
| [List Alert Integrations](actions/list-alert-integrations.md) | GET | Retrieves alert integrations from Couchbase Capella. |
| [Create Alert Integration](actions/post-alert-integration.md) | POST | Creates an alert integration in Couchbase Capella. |
| [Test Alert Integration](actions/post-test-alert-integration.md) | POST | Tests an alert integration in Couchbase Capella. |
| [Update Alert Integration](actions/put-alert-integration.md) | PUT | Updates an alert integration in Couchbase Capella. |

### Allowed Cidrs (app Services)

| Action | Method | Description |
| --- | --- | --- |
| [Delete App Service Allowed CIDR](actions/delete-app-service-allowed-cidr.md) | DELETE | Deletes an app service allowed CIDR from Couchbase Capella. |
| [List Allowed CIDRs for an App Service](actions/list-app-service-allowed-cidrs.md) | GET | Retrieves allowed CIDRs for an app service from Couchbase Capella. |
| [Create Allowed CIDR](actions/post-app-service-allowed-cidr.md) | POST | Creates an allowed CIDR in Couchbase Capella. |

### Allowed Cidrs (cluster)

| Action | Method | Description |
| --- | --- | --- |
| [Delete Allowed CIDR](actions/delete-allowed-cidr-by-id.md) | DELETE | Deletes an allowed CIDR from Couchbase Capella. |
| [get allowed CIDR](actions/get-allowed-cidr-by-id.md) | GET | Retrieves an allowed CIDR from Couchbase Capella. |
| [List Allowed CIDRs](actions/list-allowed-cidrs.md) | GET | Retrieves allowed CIDRs from Couchbase Capella. |
| [Create Allowed CIDR](actions/post-allowed-cidrs.md) | POST | Creates an allowed CIDR in Couchbase Capella. |

### Api Keys

| Action | Method | Description |
| --- | --- | --- |
| [Delete API Key](actions/delete-organization-api-key.md) | DELETE | Deletes an API key from Couchbase Capella. |
| [Get API Key](actions/get-organization-api-key-by-access-key.md) | GET | Retrieves an API key from Couchbase Capella. |
| [List API keys](actions/list-organization-api-keys.md) | GET | Retrieves API keys from Couchbase Capella. |
| [Rotate API Key](actions/post-organization-api-key-rotate.md) | POST | Rotates an API key in Couchbase Capella. |
| [Create API Key](actions/post-organization-api-keys.md) | POST | Creates an API key in Couchbase Capella. |

### App Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create App Endpoint OpenID Connect (OIDC) Provider](actions/create-app-endpoint-oidc-provider.md) | POST | Creates an app endpoint OpenID connect (OIDC) provider in Couchbase Capella. |
| [Delete Access Control and Validation function](actions/delete-access-function.md) | DELETE | Deletes an access control and validation function from Couchbase Capella. |
| [Delete App Endpoint](actions/delete-app-endpoint.md) | DELETE | Deletes an app endpoint from Couchbase Capella. |
| [Pause or Take an App Endpoint offline](actions/delete-app-endpoint-activation-status.md) | DELETE | Pauses an or take an app endpoint offline in Couchbase Capella. |
| [Delete App Endpoint OpenID Connect (OIDC) Provider](actions/delete-app-endpoint-oidc-provider.md) | DELETE | Deletes an app endpoint OpenID connect (OIDC) provider from Couchbase Capella. |
| [Stop Resync](actions/delete-app-endpoint-resync.md) | DELETE | Stops a resync in Couchbase Capella. |
| [Delete Import Filter](actions/delete-import-filter.md) | DELETE | Deletes an import filter from Couchbase Capella. |
| [Get Access Control and Validation function](actions/get-access-function.md) | GET | Retrieves an access control and validation function from Couchbase Capella. |
| [Get App Endpoint](actions/get-app-endpoint.md) | GET | Retrieves an app endpoint from Couchbase Capella. |
| [Get the App Endpoint Cross-Origin Resource Sharing (CORS) Configuration.](actions/get-app-endpoint-cors.md) | GET | Retrieves the app endpoint cross-origin resource sharing (CORS) configuration from Couchbase Capella. |
| [Get App Endpoint OpenID Connect (OIDC) Provider](actions/get-app-endpoint-oidc-provider.md) | GET | Retrieves an app endpoint OpenID connect (OIDC) provider from Couchbase Capella. |
| [Get Resync Status](actions/get-app-endpoint-resync.md) | GET | Retrieves a resync status from Couchbase Capella. |
| [Get Import Filter](actions/get-import-filter.md) | GET | Retrieves an import filter from Couchbase Capella. |
| [List App Endpoint Collections](actions/list-app-endpoint-collections.md) | GET | Retrieves app endpoint collections from Couchbase Capella. |
| [List App Endpoint OpenID Connect (OIDC) Providers](actions/list-app-endpoint-oidc-providers.md) | GET | Retrieves app endpoint OpenID connect (OIDC) providers from Couchbase Capella. |
| [List App Endpoints](actions/list-app-endpoints.md) | GET | Retrieves app endpoints from Couchbase Capella. |
| [Create App Endpoint](actions/post-app-endpoint.md) | POST | Creates an app endpoint in Couchbase Capella. |
| [Resume or Bring an App Endpoint online](actions/post-app-endpoint-activation-status.md) | POST | Resumes an or bring an app endpoint online in Couchbase Capella. |
| [Start Resync](actions/post-app-endpoint-resync.md) | POST | Starts a resync in Couchbase Capella. |
| [Upsert custom Access Control and Validation function](actions/put-access-function.md) | PUT | Upserts a custom access control and validation function in Couchbase Capella. |
| [Update App Endpoint](actions/put-app-endpoint.md) | PUT | Updates an app endpoint in Couchbase Capella. |
| [Upsert the App Endpoint Cross-Origin Resource Sharing (CORS) Configuration.](actions/put-app-endpoint-cors.md) | PUT | Upserts an app endpoint cross-origin resource sharing (CORS) configuration in Couchbase Capella. |
| [Upsert Import Filter](actions/put-import-filter.md) | PUT | Upserts an import filter in Couchbase Capella. |
| [Update App Endpoint Default OIDC Provider](actions/update-app-endpoint-oidc-default-provider.md) | PUT | Updates an app endpoint default OIDC provider in Couchbase Capella. |
| [Update App Endpoint OpenID Connect (OIDC) Provider](actions/update-app-endpoint-oidc-provider.md) | PUT | Updates an app endpoint OpenID connect (OIDC) provider in Couchbase Capella. |

### App Services

| Action | Method | Description |
| --- | --- | --- |
| [Create App Service Admin User](actions/add-app-service-admin-user.md) | POST | Creates an app service admin user in Couchbase Capella. |
| [Turn Off App Service](actions/app-service-off.md) | DELETE | Turns off an app service in Couchbase Capella. |
| [Turn On App Service](actions/app-service-on.md) | POST | Turns on an app service in Couchbase Capella. |
| [Delete App Service](actions/delete-app-service.md) | DELETE | Deletes an app service from Couchbase Capella. |
| [Delete App Service Admin User](actions/delete-app-service-admin-user.md) | DELETE | Deletes an app service admin user from Couchbase Capella. |
| [Get App Service](actions/get-app-service.md) | GET | Retrieves an app service from Couchbase Capella. |
| [Get App Service Admin User](actions/get-app-service-admin-user.md) | GET | Retrieves an app service admin user from Couchbase Capella. |
| [Get Public Certificate for App Service](actions/get-app-service-certificate.md) | GET | Retrieves a public certificate for app service from Couchbase Capella. |
| [List App Endpoint Admin Users](actions/list-app-endpoint-admin-users.md) | GET | Retrieves app endpoint admin users from Couchbase Capella. |
| [List App Service Admin Users](actions/list-app-service-admin-users.md) | GET | Retrieves app service admin users from Couchbase Capella. |
| [List AppServices](actions/list-app-services.md) | GET | Retrieves AppServices from Couchbase Capella. |
| [Create App Service](actions/post-app-service.md) | POST | Creates an app service in Couchbase Capella. |
| [Update App Service](actions/put-app-service.md) | PUT | Updates an app service in Couchbase Capella. |
| [Update App Service Admin User](actions/update-app-service-admin-user.md) | PUT | Updates an app service admin user in Couchbase Capella. |

### App Services Audit Logging

| Action | Method | Description |
| --- | --- | --- |
| [Get App Endpoint Audit Logging Config](actions/get-app-endpoint-audit-log-config.md) | GET | Retrieves an app endpoint audit logging config from Couchbase Capella. |
| [List App Endpoint Audit Log Event IDs](actions/get-app-service-audit-log-events.md) | GET | Retrieves app endpoint audit log event IDs from Couchbase Capella. |
| [Get Audit Log Export Job](actions/get-app-service-audit-log-export-by-id.md) | GET | Retrieves an audit log export job from Couchbase Capella. |
| [Get App Service Audit Log State](actions/get-app-service-audit-log-state.md) | GET | Retrieves an app service audit log state from Couchbase Capella. |
| [Get App Service Audit Log Streaming State](actions/get-app-service-audit-log-streaming.md) | GET | Retrieves an app service audit log streaming state from Couchbase Capella. |
| [List Audit Log Export Jobs](actions/list-app-service-audit-log-exports.md) | GET | Retrieves audit log export jobs from Couchbase Capella. |
| [Start or Resume Audit Log Streaming](actions/patch-app-service-audit-log-streaming.md) | PUT | Starts an or resume audit log streaming in Couchbase Capella. |
| [Initiate Audit Log Export](actions/post-app-service-audit-log-export.md) | POST | Initiates an audit log export in Couchbase Capella. |
| [Update App Endpoint Audit Logging Config](actions/put-app-endpoint-audit-log-config.md) | PUT | Updates an app endpoint audit logging config in Couchbase Capella. |
| [Enable or Disable App Service Audit Logging](actions/put-app-service-audit-log-state.md) | PUT | Enables an or disable app service audit logging in Couchbase Capella. |
| [Configure App Service Audit Log Streaming](actions/put-app-service-audit-log-streaming.md) | PUT | Configures an app service audit log streaming in Couchbase Capella. |

### App Services Log Streaming

| Action | Method | Description |
| --- | --- | --- |
| [Disable App Service Log Streaming](actions/delete-app-service-log-streaming.md) | DELETE | Disables an app service log streaming in Couchbase Capella. |
| [Get App Endpoint Log Streaming Config](actions/get-app-endpoint-log-streaming-config.md) | GET | Retrieves an app endpoint log streaming config from Couchbase Capella. |
| [Get App Service Log Streaming Configuration and State](actions/get-app-service-log-streaming.md) | GET | Retrieves an app service log streaming configuration and state from Couchbase Capella. |
| [Pause App Service Log Streaming](actions/pause-app-service-log-streaming.md) | DELETE | Pauses an app service log streaming in Couchbase Capella. |
| [Configure App Service Log Streaming](actions/post-app-service-log-streaming.md) | POST | Configures an app service log streaming in Couchbase Capella. |
| [Update App Endpoint Log Streaming Config](actions/put-app-endpoint-log-streaming-config.md) | PUT | Updates an app endpoint log streaming config in Couchbase Capella. |
| [Resume App Service Log Streaming](actions/resume-app-service-log-streaming.md) | POST | Resumes an app service log streaming in Couchbase Capella. |

### App Services Private Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Accept Private Endpoint Request](actions/accept-private-endpoint-request.md) | POST | Accepts a private endpoint request in Couchbase Capella. |
| [Disable App Service Private Endpoints](actions/delete-app-service-private-endpoints.md) | DELETE | Disables an app service private endpoints in Couchbase Capella. |
| [Delete Private Endpoint Request](actions/delete-private-endpoint-request.md) | DELETE | Deletes a private endpoint request from Couchbase Capella. |
| [Get App Service Private Endpoints State](actions/get-app-service-private-endpoints.md) | GET | Retrieves an app service private endpoints state from Couchbase Capella. |
| [Get App Service Private Endpoints Command](actions/get-app-service-private-endpoints-command.md) | POST | Retrieves an app service private endpoints command from Couchbase Capella. |
| [List App Service Private Endpoints](actions/list-app-service-private-endpoints.md) | GET | Retrieves app service private endpoints from Couchbase Capella. |
| [Enable App Service Private Endpoints](actions/post-app-service-private-endpoints.md) | POST | Enables an app service private endpoints in Couchbase Capella. |

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [List Filterable Audit Log Events](actions/get-audit-log-event-i-ds.md) | GET | Retrieves filterable audit log events from Couchbase Capella. |
| [Get Cluster Audit Log Export](actions/get-audit-log-export.md) | GET | Retrieves a cluster audit log export from Couchbase Capella. |
| [Get Cluster Audit Log Configuration](actions/get-cluster-audit-settings.md) | GET | Retrieves a cluster audit log configuration from Couchbase Capella. |
| [List Cluster Audit Log Export Jobs](actions/list-audit-log-exports.md) | GET | Retrieves cluster audit log export jobs from Couchbase Capella. |
| [Create Cluster Audit Log Export job](actions/post-audit-log-export.md) | POST | Creates a cluster audit log export job in Couchbase Capella. |
| [Update Cluster Audit Log Configuration](actions/put-cluster-audit-settings.md) | PUT | Updates a cluster audit log configuration in Couchbase Capella. |

### Backup Schedule (bucket)

| Action | Method | Description |
| --- | --- | --- |
| [Delete Backup Schedule](actions/delete-backup-schedule.md) | DELETE | Deletes a backup schedule from Couchbase Capella. |
| [Get Backup Schedule](actions/get-backup-schedule.md) | GET | Retrieves a backup schedule from Couchbase Capella. |
| [List Backups](actions/list-backups.md) | GET | Retrieves backups from Couchbase Capella. |
| [List Cycles](actions/list-cycles.md) | GET | Retrieves cycles from Couchbase Capella. |
| [Create Backup Schedule](actions/post-backup-schedule.md) | POST | Creates a backup schedule in Couchbase Capella. |
| [Update Backup Schedule](actions/put-backup-schedule.md) | PUT | Updates a backup schedule in Couchbase Capella. |

### Backups & Restore (bucket)

| Action | Method | Description |
| --- | --- | --- |
| [Delete Backup Cycle](actions/delete-backup-cycle-by-id.md) | DELETE | Deletes a backup cycle from Couchbase Capella. |
| [Get Backup](actions/get-backup-by-id.md) | GET | Retrieves a backup from Couchbase Capella. |
| [List Cluster Backups](actions/list-cluster-backups.md) | GET | Retrieves cluster backups from Couchbase Capella. |
| [Create Backup](actions/post-backup.md) | POST | Creates a backup in Couchbase Capella. |
| [Restore Backup](actions/post-restore.md) | POST | Restores a backup in Couchbase Capella. |

### Buckets, Scopes, & Collections

| Action | Method | Description |
| --- | --- | --- |
| [Delete Bucket](actions/delete-bucket-by-id.md) | DELETE | Deletes a bucket from Couchbase Capella. |
| [Delete Collection](actions/delete-collection-by-name.md) | DELETE | Deletes a collection from Couchbase Capella. |
| [Delete Scope](actions/delete-scope-by-name.md) | DELETE | Deletes a scope from Couchbase Capella. |
| [Flush Bucket Data](actions/flush-bucket.md) | PUT | Flushes a bucket data in Couchbase Capella. |
| [Get Bucket](actions/get-bucket-by-id.md) | GET | Retrieves a bucket from Couchbase Capella. |
| [Get Collection](actions/get-collection-by-name.md) | GET | Retrieves a collection from Couchbase Capella. |
| [List Collections](actions/get-collections.md) | GET | Retrieves collections from Couchbase Capella. |
| [Get Scope](actions/get-scope-by-name.md) | GET | Retrieves a scope from Couchbase Capella. |
| [List Scopes](actions/get-scopes.md) | GET | Retrieves scopes from Couchbase Capella. |
| [List Buckets](actions/list-buckets.md) | GET | Retrieves buckets from Couchbase Capella. |
| [Create Bucket](actions/post-bucket.md) | POST | Creates a bucket in Couchbase Capella. |
| [Create Collection](actions/post-collection.md) | POST | Creates a collection in Couchbase Capella. |
| [Create Scope](actions/post-scope.md) | POST | Creates a scope in Couchbase Capella. |
| [Update Bucket](actions/put-bucket.md) | PUT | Updates a bucket in Couchbase Capella. |
| [Update Collection](actions/put-collection.md) | PUT | Updates a collection in Couchbase Capella. |

### Certificates

| Action | Method | Description |
| --- | --- | --- |
| [Get Certificate](actions/get-certificate.md) | GET | Retrieves a certificate from Couchbase Capella. |

### Cloud Accounts

| Action | Method | Description |
| --- | --- | --- |
| [List Cloud Accounts](actions/list-cloud-accounts.md) | GET | Retrieves cloud accounts from Couchbase Capella. |

### Cloud Snapshot Backups & Restore

| Action | Method | Description |
| --- | --- | --- |
| [Clone Cluster Backup](actions/clone.md) | POST | Clones a cluster backup in Couchbase Capella. |
| [Create Cloud Snapshot Backup](actions/create-cloud-snapshot-backup.md) | POST | Creates a cloud snapshot backup in Couchbase Capella. |
| [Delete Backup](actions/delete-cloud-snapshot-backup.md) | DELETE | Deletes a backup from Couchbase Capella. |
| [Edit Backup Retention](actions/edit-cloud-snapshot-backup-retention.md) | PUT | Edits a backup retention in Couchbase Capella. |
| [List Cloud Snapshot Backups](actions/list-cloud-snapshot-backups.md) | GET | Retrieves cloud snapshot backups from Couchbase Capella. |
| [List Cloud Snapshot Restores](actions/list-cloud-snapshot-restores.md) | GET | Retrieves cloud snapshot restores from Couchbase Capella. |
| [List Available Geographic Regions for Cross-region Operations](actions/list-geographic-regions.md) | GET | Retrieves available geographic regions for cross-region operations from Couchbase Capella. |
| [List Cloud Snapshot Backups at the Project Level](actions/list-project-level-cloud-snapshot-backups.md) | GET | Retrieves cloud snapshot backups at the project level from Couchbase Capella. |
| [Restore Backup](actions/restore.md) | POST | Restores a backup in Couchbase Capella. |

### Cloud Snapshot Backups Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Delete Backup Schedule](actions/delete-cloud-snapshot-backup-schedule.md) | DELETE | Deletes a backup schedule from Couchbase Capella. |
| [Get Backup Schedule](actions/get-cloud-snapshot-backup-schedule.md) | GET | Retrieves a backup schedule from Couchbase Capella. |
| [Upsert Backup Schedule](actions/upsert-cloud-snapshot-backup-schedule.md) | PUT | Upserts a backup schedule in Couchbase Capella. |

### Clusters

| Action | Method | Description |
| --- | --- | --- |
| [Turn Off Cluster](actions/cluster-off.md) | DELETE | Turns off a cluster in Couchbase Capella. |
| [Turn On Cluster](actions/cluster-on.md) | POST | Turns on a cluster in Couchbase Capella. |
| [Delete Cluster](actions/delete-cluster.md) | DELETE | Deletes a cluster from Couchbase Capella. |
| [Get Cluster](actions/get-cluster.md) | GET | Retrieves a cluster from Couchbase Capella. |
| [Get Cluster Capacity Statistics](actions/get-cluster-stats.md) | GET | Retrieves a cluster capacity statistics from Couchbase Capella. |
| [List Clusters](actions/list-clusters.md) | GET | Retrieves clusters from Couchbase Capella. |
| [Create Cluster](actions/post-cluster.md) | POST | Creates a cluster in Couchbase Capella. |
| [Migrate Buckets](actions/put-bucket-storage-backend.md) | PUT | Migrates a buckets in Couchbase Capella. |
| [Update Cluster](actions/put-cluster.md) | PUT | Updates a cluster in Couchbase Capella. |

### Cmek

| Action | Method | Description |
| --- | --- | --- |
| [Associate Key with Cluster](actions/associate-cmek.md) | POST | Associates a key with cluster in Couchbase Capella. |
| [Delete Azure Key Metadata For Project](actions/delete-azure-key-metadata-for-project.md) | DELETE | Deletes an Azure key metadata for project from Couchbase Capella. |
| [Delete Key Metadata](actions/delete-key-metadata.md) | DELETE | Deletes a key metadata from Couchbase Capella. |
| [Enable CMEK For Cloud Services Provider](actions/enable-cmek.md) | PUT | Enables a CMEK for cloud services provider in Couchbase Capella. |
| [Enable Azure CMEK For Project](actions/enable-cmek-azure-project.md) | PUT | Enables an Azure CMEK for project in Couchbase Capella. |
| [Get Azure Application ID](actions/get-azure-application-id.md) | GET | Retrieves an Azure application ID from Couchbase Capella. |
| [Get Azure Application ID For Project](actions/get-azure-application-id-for-project.md) | GET | Retrieves an Azure application ID for a project from Couchbase Capella. |
| [Get Azure Key Metadata For Project](actions/get-azure-key-metadata-for-project.md) | GET | Retrieves an Azure key metadata for project from Couchbase Capella. |
| [List Azure Key Metadata For Project](actions/get-azure-key-metadata-list-for-project.md) | GET | Retrieves Azure key metadata for project from Couchbase Capella. |
| [Get Key Metadata](actions/get-key-metadata.md) | GET | Retrieves a key metadata from Couchbase Capella. |
| [List Key Metadata](actions/get-key-metadata-list.md) | GET | Retrieves key metadata from Couchbase Capella. |
| [List Key Rotation History](actions/list-cmek-history.md) | GET | Retrieves key rotation history from Couchbase Capella. |
| [Create Azure Key Metadata For Project](actions/post-cmek-azure-metadata-for-project.md) | POST | Creates an Azure key metadata for project in Couchbase Capella. |
| [Create Key Metadata](actions/post-cmek-metadata.md) | POST | Creates a key metadata in Couchbase Capella. |
| [Rotate Azure Key For Project](actions/rotate-azure-key-metadata-for-project.md) | PUT | Rotates an Azure key for project in Couchbase Capella. |
| [Rotate Key](actions/rotate-cmek-key.md) | PUT | Rotates a key in Couchbase Capella. |
| [Unassociate Key from Cluster](actions/unassociate-cmek.md) | POST | Unassociates a key from cluster in Couchbase Capella. |

### Data Api

| Action | Method | Description |
| --- | --- | --- |
| [Accept Data API Private Endpoint Connection](actions/associate-data-api-private-endpoint-request.md) | POST | Accepts a data API private endpoint connection in Couchbase Capella. |
| [Disassociate Data API Private Endpoint](actions/disassociate-data-api-private-endpoint.md) | POST | Disassociates a data API private endpoint in Couchbase Capella. |
| [Get CLI Commands For Setting Up Private Endpoint Connection](actions/get-data-api-private-endpoint-command.md) | POST | Retrieves CLI commands for a private endpoint connection from Couchbase Capella. |
| [Get Data API Status](actions/get-data-api-status.md) | GET | Retrieves Data API status from Couchbase Capella. |
| [List Data API Private Endpoints](actions/list-data-api-private-endpoints.md) | GET | Retrieves Data API private endpoints from Couchbase Capella. |
| [Update Data API](actions/update-data-api-and-peering.md) | PUT | Updates a data API in Couchbase Capella. |

### Database Credentials

| Action | Method | Description |
| --- | --- | --- |
| [Delete Database Credentials](actions/delete-database-credential.md) | DELETE | Deletes a database credentials from Couchbase Capella. |
| [Get Database Credentials](actions/get-database-credential.md) | GET | Retrieves a database credentials from Couchbase Capella. |
| [List Database Credentials](actions/list-database-credentials.md) | GET | Retrieves database credentials from Couchbase Capella. |
| [Create Database Credentials](actions/post-database-credential.md) | POST | Creates a database credentials in Couchbase Capella. |
| [Update Database Credentials](actions/put-database-credential.md) | PUT | Updates a database credentials in Couchbase Capella. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event-by-id.md) | GET | Retrieves an event from Couchbase Capella. |
| [Get Project Event](actions/get-project-event-by-id.md) | GET | Retrieves a project event from Couchbase Capella. |
| [List Events](actions/list-events.md) | GET | Retrieves events from Couchbase Capella. |
| [List Events](actions/list-project-events.md) | GET | Retrieves events from Couchbase Capella. |

### Free Tier

| Action | Method | Description |
| --- | --- | --- |
| [Create Free Tier App Service](actions/create-free-tier-app-service.md) | POST | Creates a free tier app service in Couchbase Capella. |
| [Create Free Tier Bucket](actions/create-free-tier-bucket.md) | POST | Creates a free tier bucket in Couchbase Capella. |
| [Create Free Tier Cluster](actions/create-free-tier-cluster.md) | POST | Creates a free tier cluster in Couchbase Capella. |
| [Delete Free Tier App Service](actions/delete-free-tier-app-service.md) | DELETE | Deletes a free tier app service from Couchbase Capella. |
| [Delete Free Tier Bucket](actions/delete-free-tier-bucket-by-id.md) | DELETE | Deletes a free tier bucket from Couchbase Capella. |
| [Delete Free Tier Cluster](actions/delete-free-tier-cluster.md) | DELETE | Deletes a free tier cluster from Couchbase Capella. |
| [Turn Off Free Tier Cluster](actions/free-tier-cluster-off.md) | DELETE | Turns off a free tier cluster in Couchbase Capella. |
| [Turn On Free Tier Cluster](actions/free-tier-cluster-on.md) | POST | Turns on a free tier cluster in Couchbase Capella. |
| [Get Free Tier App Service](actions/get-free-tier-app-service.md) | GET | Retrieves a free tier app service from Couchbase Capella. |
| [Get Free Tier Bucket](actions/get-free-tier-bucket-by-id.md) | GET | Retrieves a free tier bucket from Couchbase Capella. |
| [Get Free Tier Cluster](actions/get-free-tier-cluster.md) | GET | Retrieves a free tier cluster from Couchbase Capella. |
| [List Free Tier Buckets](actions/list-free-tier-buckets.md) | GET | Retrieves free tier buckets from Couchbase Capella. |
| [Update Free Tier App Service](actions/update-free-tier-app-service.md) | PUT | Updates a free tier app service in Couchbase Capella. |
| [Update Free Tier Bucket](actions/update-free-tier-bucket.md) | PUT | Updates a free tier bucket in Couchbase Capella. |
| [Update Free Tier Cluster](actions/update-free-tier-cluster.md) | PUT | Updates a free tier cluster in Couchbase Capella. |

### Model Services Api Keys (ai Services)

| Action | Method | Description |
| --- | --- | --- |
| [Create API Key](actions/create-model-api-key.md) | POST | Creates an API key in Couchbase Capella. |
| [Delete API key](actions/delete-model-api-key.md) | DELETE | Deletes an API key from Couchbase Capella. |
| [Get API Key](actions/get-model-api-key.md) | GET | Retrieves an API key from Couchbase Capella. |
| [List API keys](actions/list-model-api-keys.md) | GET | Retrieves API keys from Couchbase Capella. |

### Models (ai Services)

| Action | Method | Description |
| --- | --- | --- |
| [Create Model](actions/create-model.md) | POST | Creates a model in Couchbase Capella. |
| [Delete Model](actions/destroy-model.md) | DELETE | Deletes a model from Couchbase Capella. |
| [Get Model Connection String](actions/get-connection-string.md) | GET | Retrieves a model connection string from Couchbase Capella. |
| [Get Model](actions/get-model.md) | GET | Retrieves a model from Couchbase Capella. |
| [List Models](actions/list-models.md) | GET | Retrieves models from Couchbase Capella. |
| [Turn Off Model](actions/model-off.md) | DELETE | Turns off a model in Couchbase Capella. |
| [Turn On Model](actions/model-on.md) | POST | Turns on a model in Couchbase Capella. |
| [Update Model](actions/put-model.md) | PUT | Updates a model in Couchbase Capella. |

### Network Peers

| Action | Method | Description |
| --- | --- | --- |
| [Delete Network Peering](actions/delete-network-peering.md) | DELETE | Deletes a network peering from Couchbase Capella. |
| [Get Azure VNET Peering CLI Command](actions/get-azure-vnet-peering-command.md) | POST | Retrieves an Azure VNET peering CLI command from Couchbase Capella. |
| [Get Network Peering record](actions/get-network-peering-record.md) | GET | Retrieves a network peering record from Couchbase Capella. |
| [List Network Peering Records](actions/list-network-peering-records.md) | GET | Retrieves network peering records from Couchbase Capella. |
| [Create Network Peering](actions/post-network-peering.md) | POST | Creates a network peering in Couchbase Capella. |

### On/off Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Delete Cluster On/Off schedule](actions/delete-on-off-schedule.md) | DELETE | Deletes a cluster on/off schedule from Couchbase Capella. |
| [Get Cluster On/Off schedule](actions/get-on-off-schedule.md) | GET | Retrieves a cluster on/off schedule from Couchbase Capella. |
| [Pause Cluster On/Off Schedule](actions/pause-cluster-on-off-schedule.md) | DELETE | Pauses a cluster on/off schedule in Couchbase Capella. |
| [Create Cluster On/Off schedule](actions/post-on-off-schedule.md) | POST | Creates a cluster on/off schedule in Couchbase Capella. |
| [Update Cluster On/Off schedule](actions/put-on-off-schedule.md) | PUT | Updates a cluster on/off schedule in Couchbase Capella. |
| [Unpause Cluster On/Off Schedule](actions/unpause-cluster-on-off-schedule.md) | POST | Unpauses a cluster on/off schedule in Couchbase Capella. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from Couchbase Capella. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from Couchbase Capella. |
| [Update Organization Configuration](actions/put-organization-configuration.md) | PUT | Updates an organization configuration in Couchbase Capella. |

### Private Endpoint Service

| Action | Method | Description |
| --- | --- | --- |
| [Accept Private Endpoint Request](actions/accept-private-endpoint.md) | POST | Accepts a private endpoint request in Couchbase Capella. |
| [Reject or disassociate Private Endpoint](actions/delete-private-endpoint.md) | POST | Rejects an or disassociate private endpoint in Couchbase Capella. |
| [Disable Private Endpoint Service](actions/disable-private-endpoint-service.md) | DELETE | Disables a private endpoint service in Couchbase Capella. |
| [Enable Private Endpoint Service](actions/enable-private-endpoint-service.md) | POST | Enables a private endpoint service in Couchbase Capella. |
| [Get Private Endpoint CLI Command required to setup private endpoint for specific CSP](actions/get-private-endpoint-command.md) | POST | Retrieves a private endpoint CLI command from Couchbase Capella. |
| [Get Private Endpoint Service Status](actions/get-private-endpoint-service-status.md) | GET | Retrieves a private endpoint service status from Couchbase Capella. |
| [List Private Endpoints](actions/list-private-endpoints.md) | GET | Retrieves private endpoints from Couchbase Capella. |
| [Update Private Endpoint Service Configuration](actions/update-private-endpoint-service.md) | PUT | Updates a private endpoint service configuration in Couchbase Capella. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Delete Project](actions/delete-project-by-id.md) | DELETE | Deletes a project from Couchbase Capella. |
| [Get Project](actions/get-project-by-id.md) | GET | Retrieves a project from Couchbase Capella. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Couchbase Capella. |
| [Create Project](actions/post-project.md) | POST | Creates a project in Couchbase Capella. |
| [Update Project](actions/put-project.md) | PUT | Updates a project in Couchbase Capella. |

### Query Indexes

| Action | Method | Description |
| --- | --- | --- |
| [Get Index Build Status](actions/index-build-status.md) | GET | Retrieves an index build status from Couchbase Capella. |
| [Get Index Properties](actions/index-definition.md) | GET | Retrieves an index properties from Couchbase Capella. |
| [Get List Of Index Definitions](actions/list-index-definitions.md) | GET | Retrieves a list of index definitions from Couchbase Capella. |
| [Manage Query Indexes](actions/manage-query-indexes.md) | POST | Manages a query indexes in Couchbase Capella. |

### Replications

| Action | Method | Description |
| --- | --- | --- |
| [Create a new replication](actions/create-replication.md) | POST | Creates a new replication in Couchbase Capella. |
| [Delete a replication](actions/delete-replication.md) | DELETE | Deletes a replication from Couchbase Capella. |
| [Get replication details](actions/get-replication.md) | GET | Retrieves a replication details from Couchbase Capella. |
| [Get replication job details](actions/get-replication-job.md) | GET | Retrieves a replication job details from Couchbase Capella. |
| [List replications for a given cluster](actions/list-cluster-replications.md) | GET | Retrieves replications for a given cluster from Couchbase Capella. |
| [List replications for a given project](actions/list-project-replications.md) | GET | Retrieves replications for a given project from Couchbase Capella. |
| [Pause a replication](actions/pause-replication.md) | DELETE | Pauses a replication in Couchbase Capella. |
| [Resume a replication](actions/resume-replication.md) | POST | Resumes a replication in Couchbase Capella. |
| [Update an existing replication](actions/update-replication.md) | PUT | Updates an existing replication in Couchbase Capella. |

### Sample Bucket

| Action | Method | Description |
| --- | --- | --- |
| [Delete Sample Import Bucket](actions/delete-sample-data-by-bucket-id.md) | DELETE | Deletes a sample import bucket from Couchbase Capella. |
| [Get Sample Import Bucket](actions/get-sample-bucket-by-id.md) | GET | Retrieves a sample import bucket from Couchbase Capella. |
| [List Sample Data Import Buckets](actions/list-sample-buckets.md) | GET | Retrieves sample data import buckets from Couchbase Capella. |
| [Load Sample Data](actions/post-sample-bucket.md) | POST | Loads a sample data in Couchbase Capella. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Delete User](actions/delete-user.md) | DELETE | Deletes a user from Couchbase Capella. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Couchbase Capella. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Couchbase Capella. |
| [Update User](actions/patch-user.md) | PUT | Updates a user in Couchbase Capella. |
| [Create User](actions/post-user.md) | POST | Creates a user in Couchbase Capella. |

