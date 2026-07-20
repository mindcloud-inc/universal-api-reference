# <img src="https://images.mindcloud.co/apps/icons/microsoft-power-bi_1774553138737.png" alt="Microsoft Power BI logo" width="28" height="28"> Microsoft Power BI: Universal API

Manage Power BI workspaces, reports, dashboards, datasets, and dataflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/microsoftPowerBI/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 289
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.microsoft.com/en-us/power-platform/products/power-bi
- **Vendor API docs:** https://learn.microsoft.com/en-us/rest/api/power-bi/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (289)

### Admin

| Action | Method | Description |
| --- | --- | --- |
| [Add Power BI Encryption Key](actions/admin-add-power-bi-encryption-key.md) | POST |  |
| [Apps GetAppsAsAdmin](actions/admin-apps-getapps-as-admin.md) | GET |  |
| [Apps GetAppUsersAsAdmin](actions/admin-apps-getappusers-as-admin.md) | GET |  |
| [Capacities AssignWorkspacesToCapacity](actions/admin-capacities-assignworkspacestocapacity.md) | POST |  |
| [Capacities GetCapacityUsersAsAdmin](actions/admin-capacities-getcapacityusers-as-admin.md) | GET |  |
| [Capacities UnassignWorkspacesFromCapacity](actions/admin-capacities-unassignworkspacesfromcapacity.md) | POST |  |
| [Dashboards GetDashboardsAsAdmin](actions/admin-dashboards-getdashboards-as-admin.md) | GET |  |
| [Dashboards GetDashboardsInGroupAsAdmin](actions/admin-dashboards-getdashboards-in-group-as-admin.md) | GET |  |
| [Dashboards GetDashboardSubscriptionsAsAdmin](actions/admin-dashboards-getdashboardsubscriptions-as-admin.md) | GET |  |
| [Dashboards GetDashboardUsersAsAdmin](actions/admin-dashboards-getdashboardusers-as-admin.md) | GET |  |
| [Dashboards GetTilesAsAdmin](actions/admin-dashboards-gettiles-as-admin.md) | GET |  |
| [Dataflows ExportDataflowAsAdmin](actions/admin-dataflows-exportdataflow-as-admin.md) | GET |  |
| [Dataflows GetDataflowDatasourcesAsAdmin](actions/admin-dataflows-getdataflowdatasources-as-admin.md) | GET |  |
| [Dataflows GetDataflowsAsAdmin](actions/admin-dataflows-getdataflows-as-admin.md) | GET |  |
| [Dataflows GetDataflowsInGroupAsAdmin](actions/admin-dataflows-getdataflows-in-group-as-admin.md) | GET |  |
| [Dataflows GetDataflowUsersAsAdmin](actions/admin-dataflows-getdataflowusers-as-admin.md) | GET |  |
| [Dataflows GetUpstreamDataflowsInGroupAsAdmin](actions/admin-dataflows-getupstreamdataflows-in-group-as-admin.md) | GET |  |
| [Datasets GetDatasetsAsAdmin](actions/admin-datasets-getdatasets-as-admin.md) | GET |  |
| [Datasets GetDatasetsInGroupAsAdmin](actions/admin-datasets-getdatasets-in-group-as-admin.md) | GET |  |
| [Datasets GetDatasetToDataflowsLinksInGroupAsAdmin](actions/admin-datasets-getdatasettodataflowslinks-in-group-as-admin.md) | GET |  |
| [Datasets GetDatasetUsersAsAdmin](actions/admin-datasets-getdatasetusers-as-admin.md) | GET |  |
| [Datasets GetDatasourcesAsAdmin](actions/admin-datasets-getdatasources-as-admin.md) | GET |  |
| [Get Activity Events](actions/admin-get-activity-events.md) | GET |  |
| [Get Capacities As Admin](actions/admin-get-capacities-as-admin.md) | GET |  |
| [Get Power BI Encryption Keys](actions/admin-get-power-bi-encryption-keys.md) | GET |  |
| [Get Refreshable For Capacity](actions/admin-get-refreshable-for-capacity.md) | GET |  |
| [Get Refreshables](actions/admin-get-refreshables.md) | GET |  |
| [Get Refreshables For Capacity](actions/admin-get-refreshables-for-capacity.md) | GET |  |
| [Groups AddUserAsAdmin](actions/admin-groups-adduser-as-admin.md) | POST |  |
| [Groups DeleteUserAsAdmin](actions/admin-groups-deleteuser-as-admin.md) | DELETE |  |
| [Groups GetGroupAsAdmin](actions/admin-groups-getgroup-as-admin.md) | GET |  |
| [Groups GetGroupsAsAdmin](actions/admin-groups-getgroups-as-admin.md) | GET |  |
| [Groups GetGroupUsersAsAdmin](actions/admin-groups-getgroupusers-as-admin.md) | GET |  |
| [Groups GetUnusedArtifactsAsAdmin](actions/admin-groups-getunusedartifacts-as-admin.md) | GET |  |
| [Groups RestoreDeletedGroupAsAdmin](actions/admin-groups-restoredeletedgroup-as-admin.md) | POST |  |
| [Groups UpdateGroupAsAdmin](actions/admin-groups-updategroup-as-admin.md) | PUT |  |
| [Imports GetImportsAsAdmin](actions/admin-imports-getimports-as-admin.md) | GET |  |
| [InformationProtection RemoveLabelsAsAdmin](actions/admin-informationprotection-removelabels-as-admin.md) | POST |  |
| [InformationProtection SetLabelsAsAdmin](actions/admin-informationprotection-setlabels-as-admin.md) | POST |  |
| [Patch Capacity As Admin](actions/admin-patch-capacity-as-admin.md) | PUT |  |
| [Pipelines DeleteUserAsAdmin](actions/admin-pipelines-deleteuser-as-admin.md) | DELETE |  |
| [Pipelines GetPipelinesAsAdmin](actions/admin-pipelines-getpipelines-as-admin.md) | GET |  |
| [Pipelines GetPipelineUsersAsAdmin](actions/admin-pipelines-getpipelineusers-as-admin.md) | GET |  |
| [Pipelines UpdateUserAsAdmin](actions/admin-pipelines-updateuser-as-admin.md) | POST |  |
| [Profiles DeleteProfileAsAdmin](actions/admin-profiles-deleteprofile-as-admin.md) | DELETE |  |
| [Profiles GetProfilesAsAdmin](actions/admin-profiles-getprofiles-as-admin.md) | GET |  |
| [Reports GetReportsAsAdmin](actions/admin-reports-getreports-as-admin.md) | GET |  |
| [Reports GetReportsInGroupAsAdmin](actions/admin-reports-getreports-in-group-as-admin.md) | GET |  |
| [Reports GetReportSubscriptionsAsAdmin](actions/admin-reports-getreportsubscriptions-as-admin.md) | GET |  |
| [Reports GetReportUsersAsAdmin](actions/admin-reports-getreportusers-as-admin.md) | GET |  |
| [Rotate Power BI Encryption Key](actions/admin-rotate-power-bi-encryption-key.md) | POST |  |
| [Users GetUserArtifactAccessAsAdmin](actions/admin-users-getuserartifactaccess-as-admin.md) | GET |  |
| [Users GetUserSubscriptionsAsAdmin](actions/admin-users-getusersubscriptions-as-admin.md) | GET |  |
| [WidelySharedArtifacts LinksSharedToWholeOrganization](actions/admin-widelysharedartifacts-linkssharedtowholeorganization.md) | GET |  |
| [WidelySharedArtifacts PublishedToWeb](actions/admin-widelysharedartifacts-publishedtoweb.md) | GET |  |
| [WorkspaceInfo GetModifiedWorkspaces](actions/admin-workspaceinfo-getmodifiedworkspaces.md) | GET |  |
| [WorkspaceInfo GetScanResult](actions/admin-workspaceinfo-getscanresult.md) | GET |  |
| [WorkspaceInfo GetScanStatus](actions/admin-workspaceinfo-getscanstatus.md) | GET |  |
| [WorkspaceInfo PostWorkspaceInfo](actions/admin-workspaceinfo-postworkspaceinfo.md) | POST |  |

### Application

| Action | Method | Description |
| --- | --- | --- |
| [Get Installed App](actions/get-installed-app.md) | GET |  |
| [List Installed Apps](actions/list-installed-apps.md) | GET |  |

### Apps

| Action | Method | Description |
| --- | --- | --- |
| [Get Dashboard](actions/apps-get-dashboard.md) | GET |  |
| [Get Tile](actions/apps-get-tile.md) | GET |  |
| [Get Tiles](actions/apps-get-tiles.md) | GET |  |

### Available Features

| Action | Method | Description |
| --- | --- | --- |
| [Get Available Feature By Name](actions/available-features-get-available-feature-by-name.md) | GET |  |
| [Get Available Features](actions/available-features-get-available-features.md) | GET |  |

### Capacities

| Action | Method | Description |
| --- | --- | --- |
| [Get Capacities](actions/capacities-get-capacities.md) | GET |  |
| [Get Refreshable For Capacity](actions/capacities-get-refreshable-for-capacity.md) | GET |  |
| [Get Refreshables](actions/capacities-get-refreshables.md) | GET |  |
| [Get Refreshables For Capacity](actions/capacities-get-refreshables-for-capacity.md) | GET |  |
| [Get Workload](actions/capacities-get-workload.md) | GET |  |
| [Get Workloads](actions/capacities-get-workloads.md) | GET |  |
| [Groups AssignMyWorkspaceToCapacity](actions/capacities-groups-assignmyworkspacetocapacity.md) | POST |  |
| [Groups AssignToCapacity](actions/capacities-groups-assigntocapacity.md) | POST |  |
| [Groups CapacityAssignmentStatus](actions/capacities-groups-capacityassignmentstatus.md) | GET |  |
| [Groups CapacityAssignmentStatusMyWorkspace](actions/capacities-groups-capacityassignmentstatusmyworkspace.md) | GET |  |
| [Patch Workload](actions/capacities-patch-workload.md) | PUT |  |

### Dashboard

| Action | Method | Description |
| --- | --- | --- |
| [Add Dashboard in Workspace](actions/add-dashboard-in-workspace.md) | POST |  |
| [Delete Dashboard in Workspace](actions/delete-dashboard-in-workspace.md) | DELETE |  |
| [Get Dashboard in Workspace](actions/get-dashboard-in-workspace.md) | GET |  |
| [List Dashboards in Installed App](actions/list-dashboards-in-installed-app.md) | GET |  |
| [List Dashboards in Workspace](actions/list-dashboards-in-workspace.md) | GET |  |

### Dashboards

| Action | Method | Description |
| --- | --- | --- |
| [Add Dashboard](actions/dashboards-add-dashboard.md) | POST |  |
| [Clone Tile](actions/dashboards-clone-tile.md) | POST |  |
| [Clone Tile In Group](actions/dashboards-clone-tile-in-group.md) | POST |  |
| [Delete Dashboard](actions/dashboards-delete-dashboard.md) | DELETE |  |
| [Get Dashboard](actions/dashboards-get-dashboard.md) | GET |  |
| [Get Dashboards](actions/dashboards-get-dashboards.md) | GET |  |
| [Get Tile](actions/dashboards-get-tile.md) | GET |  |
| [Get Tiles](actions/dashboards-get-tiles.md) | GET |  |

### Data Source

| Action | Method | Description |
| --- | --- | --- |
| [List Dataset Datasources](actions/list-dataset-datasources.md) | GET |  |

### Dataflow

| Action | Method | Description |
| --- | --- | --- |
| [List Dataflows in Workspace](actions/list-dataflows-in-workspace.md) | GET |  |

### Dataflow Storage Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Get Dataflow Storage Accounts](actions/dataflow-storage-accounts-get-dataflow-storage-accounts.md) | GET |  |
| [Groups AssignToDataflowStorage](actions/dataflow-storage-accounts-groups-assigntodataflowstorage.md) | POST |  |

### Dataflows

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Dataflow Transaction](actions/dataflows-cancel-dataflow-transaction.md) | POST |  |
| [Delete Dataflow](actions/dataflows-delete-dataflow.md) | DELETE |  |
| [Get Dataflow](actions/dataflows-get-dataflow.md) | GET |  |
| [Get Dataflow Data Sources](actions/dataflows-get-dataflow-data-sources.md) | GET |  |
| [Get Dataflow Transactions](actions/dataflows-get-dataflow-transactions.md) | GET |  |
| [Get Upstream Dataflows In Group](actions/dataflows-get-upstream-dataflows-in-group.md) | GET |  |
| [Refresh Dataflow](actions/dataflows-refresh-dataflow.md) | POST |  |
| [Save Dataflow Gen One As Dataflow Gen Two](actions/dataflows-save-dataflow-gen-one-as-dataflow-gen-two.md) | POST |  |
| [Update Dataflow](actions/dataflows-update-dataflow.md) | PUT |  |
| [Update Refresh Schedule](actions/dataflows-update-refresh-schedule.md) | PUT |  |

### Dataset

| Action | Method | Description |
| --- | --- | --- |
| [Delete Dataset in Workspace](actions/delete-dataset-in-workspace.md) | DELETE |  |
| [Get Dataset in Workspace](actions/get-dataset-in-workspace.md) | GET |  |
| [List Datasets in Workspace](actions/list-datasets-in-workspace.md) | GET |  |

### Dataset Refresh

| Action | Method | Description |
| --- | --- | --- |
| [List Dataset Refresh History in Workspace](actions/list-dataset-refresh-history-in-workspace.md) | GET |  |
| [Refresh Dataset in Workspace](actions/refresh-dataset-in-workspace.md) | POST |  |

### Dataset Table Row

| Action | Method | Description |
| --- | --- | --- |
| [Add Rows to Push Dataset Table in Workspace](actions/add-rows-to-push-dataset-table-in-workspace.md) | POST |  |
| [Delete Rows from Push Dataset Table in Workspace](actions/delete-rows-from-push-dataset-table-in-workspace.md) | DELETE |  |

### Datasets

| Action | Method | Description |
| --- | --- | --- |
| [Bind To Gateway](actions/datasets-bind-to-gateway.md) | POST |  |
| [Bind To Gateway In Group](actions/datasets-bind-to-gateway-in-group.md) | POST |  |
| [Cancel Refresh](actions/datasets-cancel-refresh.md) | DELETE |  |
| [Cancel Refresh In Group](actions/datasets-cancel-refresh-in-group.md) | DELETE |  |
| [Delete Dataset](actions/datasets-delete-dataset.md) | DELETE |  |
| [Discover Gateways](actions/datasets-discover-gateways.md) | GET |  |
| [Discover Gateways In Group](actions/datasets-discover-gateways-in-group.md) | GET |  |
| [Execute Dax Queries](actions/datasets-execute-dax-queries.md) | POST |  |
| [Execute Dax Queries In Group](actions/datasets-execute-dax-queries-in-group.md) | POST |  |
| [Execute Queries](actions/datasets-execute-queries.md) | POST |  |
| [Execute Queries In Group](actions/datasets-execute-queries-in-group.md) | POST |  |
| [Get Dataset](actions/datasets-get-dataset.md) | GET |  |
| [Get Dataset To Dataflows Links In Group](actions/datasets-get-dataset-to-dataflows-links-in-group.md) | GET |  |
| [Get Dataset Users](actions/datasets-get-dataset-users.md) | GET |  |
| [Get Dataset Users In Group](actions/datasets-get-dataset-users-in-group.md) | GET |  |
| [Get Datasets](actions/datasets-get-datasets.md) | GET |  |
| [Get Datasources](actions/datasets-get-datasources.md) | GET |  |
| [Get Direct Query Refresh Schedule](actions/datasets-get-direct-query-refresh-schedule.md) | GET |  |
| [Get Direct Query Refresh Schedule In Group](actions/datasets-get-direct-query-refresh-schedule-in-group.md) | GET |  |
| [Get Gateway Datasources](actions/datasets-get-gateway-datasources.md) | GET |  |
| [Get Gateway Datasources In Group](actions/datasets-get-gateway-datasources-in-group.md) | GET |  |
| [Get Parameters](actions/datasets-get-parameters.md) | GET |  |
| [Get Parameters In Group](actions/datasets-get-parameters-in-group.md) | GET |  |
| [Get Query Scale Out Sync Status](actions/datasets-get-query-scale-out-sync-status.md) | GET |  |
| [Get Query Scale Out Sync Status In Group](actions/datasets-get-query-scale-out-sync-status-in-group.md) | GET |  |
| [Get Refresh Execution Details](actions/datasets-get-refresh-execution-details.md) | GET |  |
| [Get Refresh Execution Details In Group](actions/datasets-get-refresh-execution-details-in-group.md) | GET |  |
| [Get Refresh History](actions/datasets-get-refresh-history.md) | GET |  |
| [Get Refresh Schedule](actions/datasets-get-refresh-schedule.md) | GET |  |
| [Get Refresh Schedule In Group](actions/datasets-get-refresh-schedule-in-group.md) | GET |  |
| [Post Dataset User](actions/datasets-post-dataset-user.md) | POST |  |
| [Post Dataset User In Group](actions/datasets-post-dataset-user-in-group.md) | POST |  |
| [Put Dataset User](actions/datasets-put-dataset-user.md) | PUT |  |
| [Put Dataset User In Group](actions/datasets-put-dataset-user-in-group.md) | PUT |  |
| [Refresh Dataset](actions/datasets-refresh-dataset.md) | POST |  |
| [Set All Dataset Connections](actions/datasets-set-all-dataset-connections.md) | POST |  |
| [Set All Dataset Connections In Group](actions/datasets-set-all-dataset-connections-in-group.md) | POST |  |
| [Take Over In Group](actions/datasets-take-over-in-group.md) | POST |  |
| [Trigger Query Scale Out Sync](actions/datasets-trigger-query-scale-out-sync.md) | POST |  |
| [Trigger Query Scale Out Sync In Group](actions/datasets-trigger-query-scale-out-sync-in-group.md) | POST |  |
| [Update Dataset](actions/datasets-update-dataset.md) | PUT |  |
| [Update Dataset In Group](actions/datasets-update-dataset-in-group.md) | PUT |  |
| [Update Datasources](actions/datasets-update-datasources.md) | POST |  |
| [Update Datasources In Group](actions/datasets-update-datasources-in-group.md) | POST |  |
| [Update Direct Query Refresh Schedule](actions/datasets-update-direct-query-refresh-schedule.md) | PUT |  |
| [Update Direct Query Refresh Schedule In Group](actions/datasets-update-direct-query-refresh-schedule-in-group.md) | PUT |  |
| [Update Parameters](actions/datasets-update-parameters.md) | POST |  |
| [Update Parameters In Group](actions/datasets-update-parameters-in-group.md) | POST |  |
| [Update Refresh Schedule](actions/datasets-update-refresh-schedule.md) | PUT |  |
| [Update Refresh Schedule In Group](actions/datasets-update-refresh-schedule-in-group.md) | PUT |  |

### Embed Token

| Action | Method | Description |
| --- | --- | --- |
| [Dashboards GenerateTokenInGroup](actions/embed-token-dashboards-generatetoken-in-group.md) | POST |  |
| [Datasets GenerateTokenInGroup](actions/embed-token-datasets-generatetoken-in-group.md) | POST |  |
| [Generate Token](actions/embed-token-generate-token.md) | POST |  |
| [Reports GenerateTokenInGroup](actions/embed-token-reports-generatetoken-in-group.md) | POST |  |
| [Reports GenerateTokenForCreateInGroup](actions/embed-token-reports-generatetokenforcreate-in-group.md) | POST |  |
| [Tiles GenerateTokenInGroup](actions/embed-token-tiles-generatetoken-in-group.md) | POST |  |

### Gateways

| Action | Method | Description |
| --- | --- | --- |
| [Add Datasource User](actions/gateways-add-datasource-user.md) | POST |  |
| [Create Datasource](actions/gateways-create-datasource.md) | POST |  |
| [Delete Datasource](actions/gateways-delete-datasource.md) | DELETE |  |
| [Delete Datasource User](actions/gateways-delete-datasource-user.md) | DELETE |  |
| [Get Datasource](actions/gateways-get-datasource.md) | GET |  |
| [Get Datasource Status](actions/gateways-get-datasource-status.md) | GET |  |
| [Get Datasource Users](actions/gateways-get-datasource-users.md) | GET |  |
| [Get Datasources](actions/gateways-get-datasources.md) | GET |  |
| [Get Gateway](actions/gateways-get-gateway.md) | GET |  |
| [Get Gateways](actions/gateways-get-gateways.md) | GET |  |
| [Update Datasource](actions/gateways-update-datasource.md) | PUT |  |

### Goalnotes Preview

| Action | Method | Description |
| --- | --- | --- |
| [Delete By ID](actions/goal-notes-preview-delete-by-id.md) | DELETE |  |
| [Patch By ID](actions/goal-notes-preview-patch-by-id.md) | PUT |  |
| [Post](actions/goal-notes-preview-post.md) | POST |  |

### Goals Preview

| Action | Method | Description |
| --- | --- | --- |
| [Delete By ID](actions/goals-preview-delete-by-id.md) | DELETE |  |
| [Delete Goal Current Value Connection](actions/goals-preview-delete-goal-current-value-connection.md) | POST |  |
| [Delete Goal Target Value Connection](actions/goals-preview-delete-goal-target-value-connection.md) | POST |  |
| [Get](actions/goals-preview-get.md) | GET |  |
| [Get By ID](actions/goals-preview-get-by-id.md) | GET |  |
| [Get Refresh History](actions/goals-preview-get-refresh-history.md) | GET |  |
| [Patch By ID](actions/goals-preview-patch-by-id.md) | PUT |  |
| [Post](actions/goals-preview-post.md) | POST |  |
| [Refresh Goal Current Value](actions/goals-preview-refresh-goal-current-value.md) | POST |  |
| [Refresh Goal Target Value](actions/goals-preview-refresh-goal-target-value.md) | POST |  |

### Goalsstatusrules Preview

| Action | Method | Description |
| --- | --- | --- |
| [Delete](actions/goals-status-rules-preview-delete.md) | DELETE |  |
| [Get](actions/goals-status-rules-preview-get.md) | GET |  |
| [Post](actions/goals-status-rules-preview-post.md) | POST |  |

### Goalvalues Preview

| Action | Method | Description |
| --- | --- | --- |
| [Delete By ID](actions/goal-values-preview-delete-by-id.md) | DELETE |  |
| [Get](actions/goal-values-preview-get.md) | GET |  |
| [Get By ID](actions/goal-values-preview-get-by-id.md) | GET |  |
| [Patch By ID](actions/goal-values-preview-patch-by-id.md) | PUT |  |
| [Post](actions/goal-values-preview-post.md) | POST |  |

### Import

| Action | Method | Description |
| --- | --- | --- |
| [Get Import in Workspace](actions/get-import-in-workspace.md) | GET |  |
| [Import Excel Workbook in Workspace](actions/import-excel-workbook-in-workspace.md) | POST |  |
| [List Imports in Workspace](actions/list-imports-in-workspace.md) | GET |  |

### Imports

| Action | Method | Description |
| --- | --- | --- |
| [Create Temporary Upload Location](actions/imports-create-temporary-upload-location.md) | POST |  |
| [Create Temporary Upload Location In Group](actions/imports-create-temporary-upload-location-in-group.md) | POST |  |
| [Get Import](actions/imports-get-import.md) | GET |  |
| [Get Imports](actions/imports-get-imports.md) | GET |  |
| [Post Import](actions/imports-post-import.md) | POST |  |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Report Page](actions/get-report-page.md) | GET |  |
| [List Report Pages](actions/list-report-pages.md) | GET |  |

### Pipelines

| Action | Method | Description |
| --- | --- | --- |
| [Assign Workspace](actions/pipelines-assign-workspace.md) | POST |  |
| [Create Pipeline](actions/pipelines-create-pipeline.md) | POST |  |
| [Delete Pipeline](actions/pipelines-delete-pipeline.md) | DELETE |  |
| [Delete Pipeline User](actions/pipelines-delete-pipeline-user.md) | DELETE |  |
| [Deploy All](actions/pipelines-deploy-all.md) | POST |  |
| [Get Pipeline](actions/pipelines-get-pipeline.md) | GET |  |
| [Get Pipeline Operation](actions/pipelines-get-pipeline-operation.md) | GET |  |
| [Get Pipeline Operations](actions/pipelines-get-pipeline-operations.md) | GET |  |
| [Get Pipeline Stage Artifacts](actions/pipelines-get-pipeline-stage-artifacts.md) | GET |  |
| [Get Pipeline Stages](actions/pipelines-get-pipeline-stages.md) | GET |  |
| [Get Pipeline Users](actions/pipelines-get-pipeline-users.md) | GET |  |
| [Get Pipelines](actions/pipelines-get-pipelines.md) | GET |  |
| [Selective Deploy](actions/pipelines-selective-deploy.md) | POST |  |
| [Unassign Workspace](actions/pipelines-unassign-workspace.md) | POST |  |
| [Update Pipeline](actions/pipelines-update-pipeline.md) | PUT |  |
| [Update Pipeline User](actions/pipelines-update-pipeline-user.md) | POST |  |

### Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Create Profile](actions/profiles-create-profile.md) | POST |  |
| [Delete Profile](actions/profiles-delete-profile.md) | DELETE |  |
| [Get Profile](actions/profiles-get-profile.md) | GET |  |
| [Get Profiles](actions/profiles-get-profiles.md) | GET |  |
| [Update Profile](actions/profiles-update-profile.md) | PUT |  |

### Push Dataset

| Action | Method | Description |
| --- | --- | --- |
| [Create Push Dataset in Workspace](actions/create-push-dataset-in-workspace.md) | POST |  |

### Push Datasets

| Action | Method | Description |
| --- | --- | --- |
| [Datasets DeleteRows](actions/push-datasets-datasets-deleterows.md) | DELETE |  |
| [Datasets GetTables](actions/push-datasets-datasets-gettables.md) | GET |  |
| [Datasets GetTablesInGroup](actions/push-datasets-datasets-gettables-in-group.md) | GET |  |
| [Datasets PostDataset](actions/push-datasets-datasets-postdataset.md) | POST |  |
| [Datasets PostRows](actions/push-datasets-datasets-postrows.md) | POST |  |
| [Datasets PutTable](actions/push-datasets-datasets-puttable.md) | PUT |  |
| [Datasets PutTableInGroup](actions/push-datasets-datasets-puttable-in-group.md) | PUT |  |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Clone Report in Workspace](actions/clone-report-in-workspace.md) | POST |  |
| [Delete Report in Workspace](actions/delete-report-in-workspace.md) | DELETE |  |
| [Get Report in Installed App](actions/get-report-in-installed-app.md) | GET |  |
| [Get Report in Workspace](actions/get-report-in-workspace.md) | GET |  |
| [List Reports in Installed App](actions/list-reports-in-installed-app.md) | GET |  |
| [List Reports in Workspace](actions/list-reports-in-workspace.md) | GET |  |
| [Rebind Report in Workspace](actions/rebind-report-in-workspace.md) | PUT |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Bind To Gateway](actions/reports-bind-to-gateway.md) | POST |  |
| [Bind To Gateway In Group](actions/reports-bind-to-gateway-in-group.md) | POST |  |
| [Clone Report](actions/reports-clone-report.md) | POST |  |
| [Delete Report](actions/reports-delete-report.md) | DELETE |  |
| [Export Report](actions/reports-export-report.md) | GET |  |
| [Export Report In Group](actions/reports-export-report-in-group.md) | GET |  |
| [Export To File](actions/reports-export-to-file.md) | POST |  |
| [Export To File In Group](actions/reports-export-to-file-in-group.md) | POST |  |
| [Get Datasources](actions/reports-get-datasources.md) | GET |  |
| [Get Datasources In Group](actions/reports-get-datasources-in-group.md) | GET |  |
| [Get Export To File Status](actions/reports-get-export-to-file-status.md) | GET |  |
| [Get Export To File Status In Group](actions/reports-get-export-to-file-status-in-group.md) | GET |  |
| [Get File Of Export To File](actions/reports-get-file-of-export-to-file.md) | GET |  |
| [Get File Of Export To File In Group](actions/reports-get-file-of-export-to-file-in-group.md) | GET |  |
| [Get Page](actions/reports-get-page.md) | GET |  |
| [Get Pages](actions/reports-get-pages.md) | GET |  |
| [Get Report](actions/reports-get-report.md) | GET |  |
| [Get Reports](actions/reports-get-reports.md) | GET |  |
| [Rebind Report](actions/reports-rebind-report.md) | POST |  |
| [Take Over In Group](actions/reports-take-over-in-group.md) | POST |  |
| [Update Datasources](actions/reports-update-datasources.md) | POST |  |
| [Update Datasources In Group](actions/reports-update-datasources-in-group.md) | POST |  |
| [Update Report Content](actions/reports-update-report-content.md) | POST |  |
| [Update Report Content In Group](actions/reports-update-report-content-in-group.md) | POST |  |

### Scorecards Preview

| Action | Method | Description |
| --- | --- | --- |
| [Delete By ID](actions/scorecards-preview-delete-by-id.md) | DELETE |  |
| [Get](actions/scorecards-preview-get.md) | GET |  |
| [Get By ID](actions/scorecards-preview-get-by-id.md) | GET |  |
| [Get Scorecard By Report Id](actions/scorecards-preview-get-scorecard-by-report-id.md) | GET |  |
| [Move Goals](actions/scorecards-preview-move-goals.md) | POST |  |
| [Patch By ID](actions/scorecards-preview-patch-by-id.md) | PUT |  |
| [Post](actions/scorecards-preview-post.md) | POST |  |

### Template Apps

| Action | Method | Description |
| --- | --- | --- |
| [Create Install Ticket](actions/template-apps-create-install-ticket.md) | POST |  |

### Tile

| Action | Method | Description |
| --- | --- | --- |
| [Get Dashboard Tile](actions/get-dashboard-tile.md) | GET |  |
| [List Dashboard Tiles](actions/list-dashboard-tiles.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Workspace Users](actions/list-workspace-users.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Refresh User Permissions](actions/users-refresh-user-permissions.md) | POST |  |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace](actions/create-workspace.md) | POST |  |
| [Delete Workspace](actions/delete-workspace.md) | DELETE |  |
| [Get Workspace](actions/get-workspace.md) | GET |  |
| [List Workspaces](actions/list-workspaces.md) | GET |  |
| [Update Workspace](actions/update-workspace.md) | PUT |  |

### Workspace User

| Action | Method | Description |
| --- | --- | --- |
| [Add Workspace User](actions/add-workspace-user.md) | POST |  |
| [Delete Workspace User](actions/delete-workspace-user.md) | DELETE |  |
| [Update Workspace User](actions/update-workspace-user.md) | PUT |  |

