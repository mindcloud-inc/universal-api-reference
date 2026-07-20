# Microsoft Power BI: Native API Reference

A consolidated summary of Microsoft Power BI's API configuration and 289 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/rest/api/power-bi/
- **API base URL:** `https://api.powerbi.com/v1.0/myorg`

## Authentication

### OAuth2

Connect Power BI with Microsoft Entra delegated OAuth2.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://login.microsoftonline.com/organizations/oauth2/v2.0/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://login.microsoftonline.com/organizations/oauth2/v2.0/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `https://analysis.windows.net/powerbi/api/App.Read.All https://analysis.windows.net/powerbi/api/Dashboard.Read.All https://analysis.windows.net/powerbi/api/Dashboard.ReadWrite.All https://analysis.windows.net/powerbi/api/Dataflow.Read.All https://analysis.windows.net/powerbi/api/Dataflow.ReadWrite.All https://analysis.windows.net/powerbi/api/Dataset.Read.All https://analysis.windows.net/powerbi/api/Dataset.ReadWrite.All https://analysis.windows.net/powerbi/api/Report.Read.All https://analysis.windows.net/powerbi/api/Report.ReadWrite.All https://analysis.windows.net/powerbi/api/Workspace.Read.All https://analysis.windows.net/powerbi/api/Workspace.ReadWrite.All offline_access`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://login.microsoftonline.com/organizations/oauth2/v2.0/token.

[Official authentication documentation](https://learn.microsoft.com/en-us/power-bi/developer/embedded/register-app)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (289 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Dashboard in Workspace](actions/add-dashboard-in-workspace.md) | `POST groups/[:groupId]/dashboards` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dashboards/add-dashboard-in-group) |
| [Add Rows to Push Dataset Table in Workspace](actions/add-rows-to-push-dataset-table-in-workspace.md) | `POST groups/[:groupId]/datasets/[:datasetId]/tables/[:tableName]/rows` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/push-datasets/datasets-post-rows-in-group) |
| [Add Workspace User](actions/add-workspace-user.md) | `POST groups/[:groupId]/users` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/groups/add-group-user) |
| [Add Power BI Encryption Key](actions/admin-add-power-bi-encryption-key.md) | `POST admin/tenantKeys` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/add-power-bi-encryption-key) |
| [Apps GetAppsAsAdmin](actions/admin-apps-getapps-as-admin.md) | `GET admin/apps` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/apps-get-apps-as-admin) |
| [Apps GetAppUsersAsAdmin](actions/admin-apps-getappusers-as-admin.md) | `GET admin/apps/[:appId]/users` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/apps-get-app-users-as-admin) |
| [Capacities AssignWorkspacesToCapacity](actions/admin-capacities-assignworkspacestocapacity.md) | `POST admin/capacities/AssignWorkspaces` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/capacities-assign-workspaces-to-capacity) |
| [Capacities GetCapacityUsersAsAdmin](actions/admin-capacities-getcapacityusers-as-admin.md) | `GET admin/capacities/[:capacityId]/users` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/capacities-get-capacity-users-as-admin) |
| [Capacities UnassignWorkspacesFromCapacity](actions/admin-capacities-unassignworkspacesfromcapacity.md) | `POST admin/capacities/UnassignWorkspaces` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/capacities-unassign-workspaces-from-capacity) |
| [Dashboards GetDashboardsAsAdmin](actions/admin-dashboards-getdashboards-as-admin.md) | `GET admin/dashboards` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/dashboards-get-dashboards-as-admin) |
| [Dashboards GetDashboardsInGroupAsAdmin](actions/admin-dashboards-getdashboards-in-group-as-admin.md) | `GET admin/groups/[:groupId]/dashboards` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/dashboards-get-dashboards-in-group-as-admin) |
| [Dashboards GetDashboardSubscriptionsAsAdmin](actions/admin-dashboards-getdashboardsubscriptions-as-admin.md) | `GET admin/dashboards/[:dashboardId]/subscriptions` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/dashboards-get-dashboard-subscriptions-as-admin) |
| [Dashboards GetDashboardUsersAsAdmin](actions/admin-dashboards-getdashboardusers-as-admin.md) | `GET admin/dashboards/[:dashboardId]/users` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/dashboards-get-dashboard-users-as-admin) |
| [Dashboards GetTilesAsAdmin](actions/admin-dashboards-gettiles-as-admin.md) | `GET admin/dashboards/[:dashboardId]/tiles` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/dashboards-get-tiles-as-admin) |
| [Dataflows ExportDataflowAsAdmin](actions/admin-dataflows-exportdataflow-as-admin.md) | `GET admin/dataflows/[:dataflowId]/export` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/dataflows-export-dataflow-as-admin) |
| [Dataflows GetDataflowDatasourcesAsAdmin](actions/admin-dataflows-getdataflowdatasources-as-admin.md) | `GET admin/dataflows/[:dataflowId]/datasources` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/dataflows-get-dataflow-datasources-as-admin) |
| [Dataflows GetDataflowsAsAdmin](actions/admin-dataflows-getdataflows-as-admin.md) | `GET admin/dataflows` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/dataflows-get-dataflows-as-admin) |
| [Dataflows GetDataflowsInGroupAsAdmin](actions/admin-dataflows-getdataflows-in-group-as-admin.md) | `GET admin/groups/[:groupId]/dataflows` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/dataflows-get-dataflows-in-group-as-admin) |
| [Dataflows GetDataflowUsersAsAdmin](actions/admin-dataflows-getdataflowusers-as-admin.md) | `GET admin/dataflows/[:dataflowId]/users` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/dataflows-get-dataflow-users-as-admin) |
| [Dataflows GetUpstreamDataflowsInGroupAsAdmin](actions/admin-dataflows-getupstreamdataflows-in-group-as-admin.md) | `GET admin/groups/[:groupId]/dataflows/[:dataflowId]/upstreamDataflows` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/dataflows-get-upstream-dataflows-in-group-as-admin) |
| [Datasets GetDatasetsAsAdmin](actions/admin-datasets-getdatasets-as-admin.md) | `GET admin/datasets` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/datasets-get-datasets-as-admin) |
| [Datasets GetDatasetsInGroupAsAdmin](actions/admin-datasets-getdatasets-in-group-as-admin.md) | `GET admin/groups/[:groupId]/datasets` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/datasets-get-datasets-in-group-as-admin) |
| [Datasets GetDatasetToDataflowsLinksInGroupAsAdmin](actions/admin-datasets-getdatasettodataflowslinks-in-group-as-admin.md) | `GET admin/groups/[:groupId]/datasets/upstreamDataflows` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/datasets-get-dataset-to-dataflows-links-in-group-as-admin) |
| [Datasets GetDatasetUsersAsAdmin](actions/admin-datasets-getdatasetusers-as-admin.md) | `GET admin/datasets/[:datasetId]/users` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/datasets-get-dataset-users-as-admin) |
| [Datasets GetDatasourcesAsAdmin](actions/admin-datasets-getdatasources-as-admin.md) | `GET admin/datasets/[:datasetId]/datasources` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/datasets-get-datasources-as-admin) |
| [Get Activity Events](actions/admin-get-activity-events.md) | `GET admin/activityevents` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/get-activity-events) |
| [Get Capacities As Admin](actions/admin-get-capacities-as-admin.md) | `GET admin/capacities` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/get-capacities-as-admin) |
| [Get Power BI Encryption Keys](actions/admin-get-power-bi-encryption-keys.md) | `GET admin/tenantKeys` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/get-power-bi-encryption-keys) |
| [Get Refreshable For Capacity](actions/admin-get-refreshable-for-capacity.md) | `GET admin/capacities/[:capacityId]/refreshables/[:refreshableId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/get-refreshable-for-capacity) |
| [Get Refreshables](actions/admin-get-refreshables.md) | `GET admin/capacities/refreshables` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/get-refreshables) |
| [Get Refreshables For Capacity](actions/admin-get-refreshables-for-capacity.md) | `GET admin/capacities/[:capacityId]/refreshables` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/get-refreshables-for-capacity) |
| [Groups AddUserAsAdmin](actions/admin-groups-adduser-as-admin.md) | `POST admin/groups/[:groupId]/users` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/groups-add-user-as-admin) |
| [Groups DeleteUserAsAdmin](actions/admin-groups-deleteuser-as-admin.md) | `DELETE admin/groups/[:groupId]/users/[:user]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/groups-delete-user-as-admin) |
| [Groups GetGroupAsAdmin](actions/admin-groups-getgroup-as-admin.md) | `GET admin/groups/[:groupId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/groups-get-group-as-admin) |
| [Groups GetGroupsAsAdmin](actions/admin-groups-getgroups-as-admin.md) | `GET admin/groups` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/groups-get-groups-as-admin) |
| [Groups GetGroupUsersAsAdmin](actions/admin-groups-getgroupusers-as-admin.md) | `GET admin/groups/[:groupId]/users` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/groups-get-group-users-as-admin) |
| [Groups GetUnusedArtifactsAsAdmin](actions/admin-groups-getunusedartifacts-as-admin.md) | `GET admin/groups/[:groupId]/unused` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/groups-get-unused-artifacts-as-admin) |
| [Groups RestoreDeletedGroupAsAdmin](actions/admin-groups-restoredeletedgroup-as-admin.md) | `POST admin/groups/[:groupId]/restore` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/groups-restore-deleted-group-as-admin) |
| [Groups UpdateGroupAsAdmin](actions/admin-groups-updategroup-as-admin.md) | `PATCH admin/groups/[:groupId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/groups-update-group-as-admin) |
| [Imports GetImportsAsAdmin](actions/admin-imports-getimports-as-admin.md) | `GET admin/imports` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/imports-get-imports-as-admin) |
| [InformationProtection RemoveLabelsAsAdmin](actions/admin-informationprotection-removelabels-as-admin.md) | `POST admin/informationprotection/removeLabels` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/information-protection-remove-labels-as-admin) |
| [InformationProtection SetLabelsAsAdmin](actions/admin-informationprotection-setlabels-as-admin.md) | `POST admin/informationprotection/setLabels` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/information-protection-set-labels-as-admin) |
| [Patch Capacity As Admin](actions/admin-patch-capacity-as-admin.md) | `PATCH admin/capacities/[:capacityId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/patch-capacity-as-admin) |
| [Pipelines DeleteUserAsAdmin](actions/admin-pipelines-deleteuser-as-admin.md) | `DELETE admin/pipelines/[:pipelineId]/users/[:identifier]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/pipelines-delete-user-as-admin) |
| [Pipelines GetPipelinesAsAdmin](actions/admin-pipelines-getpipelines-as-admin.md) | `GET admin/pipelines` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/pipelines-get-pipelines-as-admin) |
| [Pipelines GetPipelineUsersAsAdmin](actions/admin-pipelines-getpipelineusers-as-admin.md) | `GET admin/pipelines/[:pipelineId]/users` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/pipelines-get-pipeline-users-as-admin) |
| [Pipelines UpdateUserAsAdmin](actions/admin-pipelines-updateuser-as-admin.md) | `POST admin/pipelines/[:pipelineId]/users` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/pipelines-update-user-as-admin) |
| [Profiles DeleteProfileAsAdmin](actions/admin-profiles-deleteprofile-as-admin.md) | `DELETE admin/profiles/[:profileId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/profiles-delete-profile-as-admin) |
| [Profiles GetProfilesAsAdmin](actions/admin-profiles-getprofiles-as-admin.md) | `GET admin/profiles` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/profiles-get-profiles-as-admin) |
| [Reports GetReportsAsAdmin](actions/admin-reports-getreports-as-admin.md) | `GET admin/reports` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/reports-get-reports-as-admin) |
| [Reports GetReportsInGroupAsAdmin](actions/admin-reports-getreports-in-group-as-admin.md) | `GET admin/groups/[:groupId]/reports` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/reports-get-reports-in-group-as-admin) |
| [Reports GetReportSubscriptionsAsAdmin](actions/admin-reports-getreportsubscriptions-as-admin.md) | `GET admin/reports/[:reportId]/subscriptions` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/reports-get-report-subscriptions-as-admin) |
| [Reports GetReportUsersAsAdmin](actions/admin-reports-getreportusers-as-admin.md) | `GET admin/reports/[:reportId]/users` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/reports-get-report-users-as-admin) |
| [Rotate Power BI Encryption Key](actions/admin-rotate-power-bi-encryption-key.md) | `POST admin/tenantKeys/[:tenantKeyId]/Default.Rotate` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/rotate-power-bi-encryption-key) |
| [Users GetUserArtifactAccessAsAdmin](actions/admin-users-getuserartifactaccess-as-admin.md) | `GET admin/users/[:userId]/artifactAccess` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/users-get-user-artifact-access-as-admin) |
| [Users GetUserSubscriptionsAsAdmin](actions/admin-users-getusersubscriptions-as-admin.md) | `GET admin/users/[:userId]/subscriptions` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/users-get-user-subscriptions-as-admin) |
| [WidelySharedArtifacts LinksSharedToWholeOrganization](actions/admin-widelysharedartifacts-linkssharedtowholeorganization.md) | `GET admin/widelySharedArtifacts/linksSharedToWholeOrganization` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/widely-shared-artifacts-links-shared-to-whole-organization) |
| [WidelySharedArtifacts PublishedToWeb](actions/admin-widelysharedartifacts-publishedtoweb.md) | `GET admin/widelySharedArtifacts/publishedToWeb` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/widely-shared-artifacts-published-to-web) |
| [WorkspaceInfo GetModifiedWorkspaces](actions/admin-workspaceinfo-getmodifiedworkspaces.md) | `GET admin/workspaces/modified` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/workspace-info-get-modified-workspaces) |
| [WorkspaceInfo GetScanResult](actions/admin-workspaceinfo-getscanresult.md) | `GET admin/workspaces/scanResult/[:scanId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/workspace-info-get-scan-result) |
| [WorkspaceInfo GetScanStatus](actions/admin-workspaceinfo-getscanstatus.md) | `GET admin/workspaces/scanStatus/[:scanId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/workspace-info-get-scan-status) |
| [WorkspaceInfo PostWorkspaceInfo](actions/admin-workspaceinfo-postworkspaceinfo.md) | `POST admin/workspaces/getInfo` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/workspace-info-post-workspace-info) |
| [Get Dashboard](actions/apps-get-dashboard.md) | `GET apps/[:appId]/dashboards/[:dashboardId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/apps/get-dashboard) |
| [Get Tile](actions/apps-get-tile.md) | `GET apps/[:appId]/dashboards/[:dashboardId]/tiles/[:tileId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/apps/get-tile) |
| [Get Tiles](actions/apps-get-tiles.md) | `GET apps/[:appId]/dashboards/[:dashboardId]/tiles` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/apps/get-tiles) |
| [Get Available Feature By Name](actions/available-features-get-available-feature-by-name.md) | `GET availableFeatures(featureName='[:featureName]')` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/available-features/get-available-feature-by-name) |
| [Get Available Features](actions/available-features-get-available-features.md) | `GET availableFeatures` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/available-features/get-available-features) |
| [Get Capacities](actions/capacities-get-capacities.md) | `GET capacities` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/capacities/get-capacities) |
| [Get Refreshable For Capacity](actions/capacities-get-refreshable-for-capacity.md) | `GET capacities/[:capacityId]/refreshables/[:refreshableId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/capacities/get-refreshable-for-capacity) |
| [Get Refreshables](actions/capacities-get-refreshables.md) | `GET capacities/refreshables` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/capacities/get-refreshables) |
| [Get Refreshables For Capacity](actions/capacities-get-refreshables-for-capacity.md) | `GET capacities/[:capacityId]/refreshables` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/capacities/get-refreshables-for-capacity) |
| [Get Workload](actions/capacities-get-workload.md) | `GET capacities/[:capacityId]/Workloads/[:workloadName]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/capacities/get-workload) |
| [Get Workloads](actions/capacities-get-workloads.md) | `GET capacities/[:capacityId]/Workloads` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/capacities/get-workloads) |
| [Groups AssignMyWorkspaceToCapacity](actions/capacities-groups-assignmyworkspacetocapacity.md) | `POST AssignToCapacity` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/capacities/groups-assign-my-workspace-to-capacity) |
| [Groups AssignToCapacity](actions/capacities-groups-assigntocapacity.md) | `POST groups/[:groupId]/AssignToCapacity` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/capacities/groups-assign-to-capacity) |
| [Groups CapacityAssignmentStatus](actions/capacities-groups-capacityassignmentstatus.md) | `GET groups/[:groupId]/CapacityAssignmentStatus` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/capacities/groups-capacity-assignment-status) |
| [Groups CapacityAssignmentStatusMyWorkspace](actions/capacities-groups-capacityassignmentstatusmyworkspace.md) | `GET CapacityAssignmentStatus` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/capacities/groups-capacity-assignment-status-my-workspace) |
| [Patch Workload](actions/capacities-patch-workload.md) | `PATCH capacities/[:capacityId]/Workloads/[:workloadName]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/capacities/patch-workload) |
| [Clone Report in Workspace](actions/clone-report-in-workspace.md) | `POST groups/[:groupId]/reports/[:reportId]/Clone` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/clone-report-in-group) |
| [Create Push Dataset in Workspace](actions/create-push-dataset-in-workspace.md) | `POST groups/[:groupId]/datasets` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/push-datasets/datasets-post-dataset-in-group) |
| [Create Workspace](actions/create-workspace.md) | `POST groups` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/groups/create-group) |
| [Add Dashboard](actions/dashboards-add-dashboard.md) | `POST dashboards` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dashboards/add-dashboard) |
| [Clone Tile](actions/dashboards-clone-tile.md) | `POST dashboards/[:dashboardId]/tiles/[:tileId]/Clone` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dashboards/clone-tile) |
| [Clone Tile In Group](actions/dashboards-clone-tile-in-group.md) | `POST groups/[:groupId]/dashboards/[:dashboardId]/tiles/[:tileId]/Clone` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dashboards/clone-tile-in-group) |
| [Delete Dashboard](actions/dashboards-delete-dashboard.md) | `DELETE dashboards/[:dashboardId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dashboards/delete-dashboard) |
| [Get Dashboard](actions/dashboards-get-dashboard.md) | `GET dashboards/[:dashboardId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dashboards/get-dashboard) |
| [Get Dashboards](actions/dashboards-get-dashboards.md) | `GET dashboards` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dashboards/get-dashboards) |
| [Get Tile](actions/dashboards-get-tile.md) | `GET dashboards/[:dashboardId]/tiles/[:tileId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dashboards/get-tile) |
| [Get Tiles](actions/dashboards-get-tiles.md) | `GET dashboards/[:dashboardId]/tiles` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dashboards/get-tiles) |
| [Get Dataflow Storage Accounts](actions/dataflow-storage-accounts-get-dataflow-storage-accounts.md) | `GET dataflowStorageAccounts` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dataflow-storage-accounts/get-dataflow-storage-accounts) |
| [Groups AssignToDataflowStorage](actions/dataflow-storage-accounts-groups-assigntodataflowstorage.md) | `POST groups/[:groupId]/AssignToDataflowStorage` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dataflow-storage-accounts/groups-assign-to-dataflow-storage) |
| [Cancel Dataflow Transaction](actions/dataflows-cancel-dataflow-transaction.md) | `POST groups/[:groupId]/dataflows/transactions/[:transactionId]/cancel` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dataflows/cancel-dataflow-transaction) |
| [Delete Dataflow](actions/dataflows-delete-dataflow.md) | `DELETE groups/[:groupId]/dataflows/[:dataflowId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dataflows/delete-dataflow) |
| [Get Dataflow](actions/dataflows-get-dataflow.md) | `GET groups/[:groupId]/dataflows/[:dataflowId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dataflows/get-dataflow) |
| [Get Dataflow Data Sources](actions/dataflows-get-dataflow-data-sources.md) | `GET groups/[:groupId]/dataflows/[:dataflowId]/datasources` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dataflows/get-dataflow-data-sources) |
| [Get Dataflow Transactions](actions/dataflows-get-dataflow-transactions.md) | `GET groups/[:groupId]/dataflows/[:dataflowId]/transactions` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dataflows/get-dataflow-transactions) |
| [Get Upstream Dataflows In Group](actions/dataflows-get-upstream-dataflows-in-group.md) | `GET groups/[:groupId]/dataflows/[:dataflowId]/upstreamDataflows` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dataflows/get-upstream-dataflows-in-group) |
| [Refresh Dataflow](actions/dataflows-refresh-dataflow.md) | `POST groups/[:groupId]/dataflows/[:dataflowId]/refreshes` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dataflows/refresh-dataflow) |
| [Save Dataflow Gen One As Dataflow Gen Two](actions/dataflows-save-dataflow-gen-one-as-dataflow-gen-two.md) | `POST groups/[:groupId]/dataflows/[:gen1DataflowId]/saveAsNativeArtifact` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dataflows/save-dataflow-gen-one-as-dataflow-gen-two) |
| [Update Dataflow](actions/dataflows-update-dataflow.md) | `PATCH groups/[:groupId]/dataflows/[:dataflowId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dataflows/update-dataflow) |
| [Update Refresh Schedule](actions/dataflows-update-refresh-schedule.md) | `PATCH groups/[:groupId]/dataflows/[:dataflowId]/refreshSchedule` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dataflows/update-refresh-schedule) |
| [Bind To Gateway](actions/datasets-bind-to-gateway.md) | `POST datasets/[:datasetId]/Default.BindToGateway` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/bind-to-gateway) |
| [Bind To Gateway In Group](actions/datasets-bind-to-gateway-in-group.md) | `POST groups/[:groupId]/datasets/[:datasetId]/Default.BindToGateway` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/bind-to-gateway-in-group) |
| [Cancel Refresh](actions/datasets-cancel-refresh.md) | `DELETE datasets/[:datasetId]/refreshes/[:refreshId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/cancel-refresh) |
| [Cancel Refresh In Group](actions/datasets-cancel-refresh-in-group.md) | `DELETE groups/[:groupId]/datasets/[:datasetId]/refreshes/[:refreshId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/cancel-refresh-in-group) |
| [Delete Dataset](actions/datasets-delete-dataset.md) | `DELETE datasets/[:datasetId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/delete-dataset) |
| [Discover Gateways](actions/datasets-discover-gateways.md) | `GET datasets/[:datasetId]/Default.DiscoverGateways` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/discover-gateways) |
| [Discover Gateways In Group](actions/datasets-discover-gateways-in-group.md) | `GET groups/[:groupId]/datasets/[:datasetId]/Default.DiscoverGateways` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/discover-gateways-in-group) |
| [Execute Dax Queries](actions/datasets-execute-dax-queries.md) | `POST datasets/[:datasetId]/executeDaxQueries` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/execute-dax-queries) |
| [Execute Dax Queries In Group](actions/datasets-execute-dax-queries-in-group.md) | `POST groups/[:groupId]/datasets/[:datasetId]/executeDaxQueries` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/execute-dax-queries-in-group) |
| [Execute Queries](actions/datasets-execute-queries.md) | `POST datasets/[:datasetId]/executeQueries` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/execute-queries) |
| [Execute Queries In Group](actions/datasets-execute-queries-in-group.md) | `POST groups/[:groupId]/datasets/[:datasetId]/executeQueries` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/execute-queries-in-group) |
| [Get Dataset](actions/datasets-get-dataset.md) | `GET datasets/[:datasetId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-dataset) |
| [Get Dataset To Dataflows Links In Group](actions/datasets-get-dataset-to-dataflows-links-in-group.md) | `GET groups/[:groupId]/datasets/upstreamDataflows` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-dataset-to-dataflows-links-in-group) |
| [Get Dataset Users](actions/datasets-get-dataset-users.md) | `GET datasets/[:datasetId]/users` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-dataset-users) |
| [Get Dataset Users In Group](actions/datasets-get-dataset-users-in-group.md) | `GET groups/[:groupId]/datasets/[:datasetId]/users` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-dataset-users-in-group) |
| [Get Datasets](actions/datasets-get-datasets.md) | `GET datasets` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-datasets) |
| [Get Datasources](actions/datasets-get-datasources.md) | `GET datasets/[:datasetId]/datasources` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-datasources) |
| [Get Direct Query Refresh Schedule](actions/datasets-get-direct-query-refresh-schedule.md) | `GET datasets/[:datasetId]/directQueryRefreshSchedule` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-direct-query-refresh-schedule) |
| [Get Direct Query Refresh Schedule In Group](actions/datasets-get-direct-query-refresh-schedule-in-group.md) | `GET groups/[:groupId]/datasets/[:datasetId]/directQueryRefreshSchedule` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-direct-query-refresh-schedule-in-group) |
| [Get Gateway Datasources](actions/datasets-get-gateway-datasources.md) | `GET datasets/[:datasetId]/Default.GetBoundGatewayDatasources` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-gateway-datasources) |
| [Get Gateway Datasources In Group](actions/datasets-get-gateway-datasources-in-group.md) | `GET groups/[:groupId]/datasets/[:datasetId]/Default.GetBoundGatewayDatasources` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-gateway-datasources-in-group) |
| [Get Parameters](actions/datasets-get-parameters.md) | `GET datasets/[:datasetId]/parameters` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-parameters) |
| [Get Parameters In Group](actions/datasets-get-parameters-in-group.md) | `GET groups/[:groupId]/datasets/[:datasetId]/parameters` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-parameters-in-group) |
| [Get Query Scale Out Sync Status](actions/datasets-get-query-scale-out-sync-status.md) | `GET datasets/[:datasetId]/queryScaleOut/syncStatus` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-query-scale-out-sync-status) |
| [Get Query Scale Out Sync Status In Group](actions/datasets-get-query-scale-out-sync-status-in-group.md) | `GET groups/[:groupId]/datasets/[:datasetId]/queryScaleOut/syncStatus` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-query-scale-out-sync-status-in-group) |
| [Get Refresh Execution Details](actions/datasets-get-refresh-execution-details.md) | `GET datasets/[:datasetId]/refreshes/[:refreshId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-refresh-execution-details) |
| [Get Refresh Execution Details In Group](actions/datasets-get-refresh-execution-details-in-group.md) | `GET groups/[:groupId]/datasets/[:datasetId]/refreshes/[:refreshId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-refresh-execution-details-in-group) |
| [Get Refresh History](actions/datasets-get-refresh-history.md) | `GET datasets/[:datasetId]/refreshes` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-refresh-history) |
| [Get Refresh Schedule](actions/datasets-get-refresh-schedule.md) | `GET datasets/[:datasetId]/refreshSchedule` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-refresh-schedule) |
| [Get Refresh Schedule In Group](actions/datasets-get-refresh-schedule-in-group.md) | `GET groups/[:groupId]/datasets/[:datasetId]/refreshSchedule` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-refresh-schedule-in-group) |
| [Post Dataset User](actions/datasets-post-dataset-user.md) | `POST datasets/[:datasetId]/users` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/post-dataset-user) |
| [Post Dataset User In Group](actions/datasets-post-dataset-user-in-group.md) | `POST groups/[:groupId]/datasets/[:datasetId]/users` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/post-dataset-user-in-group) |
| [Put Dataset User](actions/datasets-put-dataset-user.md) | `PUT datasets/[:datasetId]/users` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/put-dataset-user) |
| [Put Dataset User In Group](actions/datasets-put-dataset-user-in-group.md) | `PUT groups/[:groupId]/datasets/[:datasetId]/users` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/put-dataset-user-in-group) |
| [Refresh Dataset](actions/datasets-refresh-dataset.md) | `POST datasets/[:datasetId]/refreshes` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/refresh-dataset) |
| [Set All Dataset Connections](actions/datasets-set-all-dataset-connections.md) | `POST datasets/[:datasetId]/Default.SetAllConnections` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/set-all-dataset-connections) |
| [Set All Dataset Connections In Group](actions/datasets-set-all-dataset-connections-in-group.md) | `POST groups/[:groupId]/datasets/[:datasetId]/Default.SetAllConnections` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/set-all-dataset-connections-in-group) |
| [Take Over In Group](actions/datasets-take-over-in-group.md) | `POST groups/[:groupId]/datasets/[:datasetId]/Default.TakeOver` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/take-over-in-group) |
| [Trigger Query Scale Out Sync](actions/datasets-trigger-query-scale-out-sync.md) | `POST datasets/[:datasetId]/queryScaleOut/sync` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/trigger-query-scale-out-sync) |
| [Trigger Query Scale Out Sync In Group](actions/datasets-trigger-query-scale-out-sync-in-group.md) | `POST groups/[:groupId]/datasets/[:datasetId]/queryScaleOut/sync` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/trigger-query-scale-out-sync-in-group) |
| [Update Dataset](actions/datasets-update-dataset.md) | `PATCH datasets/[:datasetId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/update-dataset) |
| [Update Dataset In Group](actions/datasets-update-dataset-in-group.md) | `PATCH groups/[:groupId]/datasets/[:datasetId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/update-dataset-in-group) |
| [Update Datasources](actions/datasets-update-datasources.md) | `POST datasets/[:datasetId]/Default.UpdateDatasources` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/update-datasources) |
| [Update Datasources In Group](actions/datasets-update-datasources-in-group.md) | `POST groups/[:groupId]/datasets/[:datasetId]/Default.UpdateDatasources` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/update-datasources-in-group) |
| [Update Direct Query Refresh Schedule](actions/datasets-update-direct-query-refresh-schedule.md) | `PATCH datasets/[:datasetId]/directQueryRefreshSchedule` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/update-direct-query-refresh-schedule) |
| [Update Direct Query Refresh Schedule In Group](actions/datasets-update-direct-query-refresh-schedule-in-group.md) | `PATCH groups/[:groupId]/datasets/[:datasetId]/directQueryRefreshSchedule` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/update-direct-query-refresh-schedule-in-group) |
| [Update Parameters](actions/datasets-update-parameters.md) | `POST datasets/[:datasetId]/Default.UpdateParameters` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/update-parameters) |
| [Update Parameters In Group](actions/datasets-update-parameters-in-group.md) | `POST groups/[:groupId]/datasets/[:datasetId]/Default.UpdateParameters` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/update-parameters-in-group) |
| [Update Refresh Schedule](actions/datasets-update-refresh-schedule.md) | `PATCH datasets/[:datasetId]/refreshSchedule` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/update-refresh-schedule) |
| [Update Refresh Schedule In Group](actions/datasets-update-refresh-schedule-in-group.md) | `PATCH groups/[:groupId]/datasets/[:datasetId]/refreshSchedule` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/update-refresh-schedule-in-group) |
| [Delete Dashboard in Workspace](actions/delete-dashboard-in-workspace.md) | `DELETE groups/[:groupId]/dashboards/[:dashboardId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dashboards/delete-dashboard-in-group) |
| [Delete Dataset in Workspace](actions/delete-dataset-in-workspace.md) | `DELETE groups/[:groupId]/datasets/[:datasetId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/delete-dataset-in-group) |
| [Delete Report in Workspace](actions/delete-report-in-workspace.md) | `DELETE groups/[:groupId]/reports/[:reportId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/delete-report-in-group) |
| [Delete Rows from Push Dataset Table in Workspace](actions/delete-rows-from-push-dataset-table-in-workspace.md) | `DELETE groups/[:groupId]/datasets/[:datasetId]/tables/[:tableName]/rows` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/push-datasets/datasets-delete-rows-in-group) |
| [Delete Workspace](actions/delete-workspace.md) | `DELETE groups/[:groupId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/groups/delete-group) |
| [Delete Workspace User](actions/delete-workspace-user.md) | `DELETE groups/[:groupId]/users/[:user]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/groups/delete-user-in-group) |
| [Dashboards GenerateTokenInGroup](actions/embed-token-dashboards-generatetoken-in-group.md) | `POST groups/[:groupId]/dashboards/[:dashboardId]/GenerateToken` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/embed-token/dashboards-generate-token-in-group) |
| [Datasets GenerateTokenInGroup](actions/embed-token-datasets-generatetoken-in-group.md) | `POST groups/[:groupId]/datasets/[:datasetId]/GenerateToken` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/embed-token/datasets-generate-token-in-group) |
| [Generate Token](actions/embed-token-generate-token.md) | `POST GenerateToken` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/embed-token/generate-token) |
| [Reports GenerateTokenInGroup](actions/embed-token-reports-generatetoken-in-group.md) | `POST groups/[:groupId]/reports/[:reportId]/GenerateToken` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/embed-token/reports-generate-token-in-group) |
| [Reports GenerateTokenForCreateInGroup](actions/embed-token-reports-generatetokenforcreate-in-group.md) | `POST groups/[:groupId]/reports/GenerateToken` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/embed-token/reports-generate-token-for-create-in-group) |
| [Tiles GenerateTokenInGroup](actions/embed-token-tiles-generatetoken-in-group.md) | `POST groups/[:groupId]/dashboards/[:dashboardId]/tiles/[:tileId]/GenerateToken` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/embed-token/tiles-generate-token-in-group) |
| [Add Datasource User](actions/gateways-add-datasource-user.md) | `POST gateways/[:gatewayId]/datasources/[:datasourceId]/users` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/gateways/add-datasource-user) |
| [Create Datasource](actions/gateways-create-datasource.md) | `POST gateways/[:gatewayId]/datasources` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/gateways/create-datasource) |
| [Delete Datasource](actions/gateways-delete-datasource.md) | `DELETE gateways/[:gatewayId]/datasources/[:datasourceId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/gateways/delete-datasource) |
| [Delete Datasource User](actions/gateways-delete-datasource-user.md) | `DELETE gateways/[:gatewayId]/datasources/[:datasourceId]/users/[:emailAdress]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/gateways/delete-datasource-user) |
| [Get Datasource](actions/gateways-get-datasource.md) | `GET gateways/[:gatewayId]/datasources/[:datasourceId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/gateways/get-datasource) |
| [Get Datasource Status](actions/gateways-get-datasource-status.md) | `GET gateways/[:gatewayId]/datasources/[:datasourceId]/status` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/gateways/get-datasource-status) |
| [Get Datasource Users](actions/gateways-get-datasource-users.md) | `GET gateways/[:gatewayId]/datasources/[:datasourceId]/users` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/gateways/get-datasource-users) |
| [Get Datasources](actions/gateways-get-datasources.md) | `GET gateways/[:gatewayId]/datasources` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/gateways/get-datasources) |
| [Get Gateway](actions/gateways-get-gateway.md) | `GET gateways/[:gatewayId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/gateways/get-gateway) |
| [Get Gateways](actions/gateways-get-gateways.md) | `GET gateways` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/gateways/get-gateways) |
| [Update Datasource](actions/gateways-update-datasource.md) | `PATCH gateways/[:gatewayId]/datasources/[:datasourceId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/gateways/update-datasource) |
| [Get Dashboard in Workspace](actions/get-dashboard-in-workspace.md) | `GET groups/[:groupId]/dashboards/[:dashboardId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dashboards/get-dashboard-in-group) |
| [Get Dashboard Tile](actions/get-dashboard-tile.md) | `GET groups/[:groupId]/dashboards/[:dashboardId]/tiles/[:tileId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dashboards/get-tile-in-group) |
| [Get Dataset in Workspace](actions/get-dataset-in-workspace.md) | `GET groups/[:groupId]/datasets/[:datasetId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-dataset-in-group) |
| [Get Import in Workspace](actions/get-import-in-workspace.md) | `GET groups/[:groupId]/imports/[:importId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/imports/get-import-in-group) |
| [Get Installed App](actions/get-installed-app.md) | `GET apps/[:appId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/apps/get-app) |
| [Get Report in Installed App](actions/get-report-in-installed-app.md) | `GET apps/[:appId]/reports/[:reportId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/apps/get-report) |
| [Get Report in Workspace](actions/get-report-in-workspace.md) | `GET groups/[:groupId]/reports/[:reportId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/get-report-in-group) |
| [Get Report Page](actions/get-report-page.md) | `GET groups/[:groupId]/reports/[:reportId]/pages/[:pageName]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/get-page-in-group) |
| [Get Workspace](actions/get-workspace.md) | `GET groups/[:groupId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/groups/get-group) |
| [Delete By ID](actions/goal-notes-preview-delete-by-id.md) | `DELETE groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/goalValues([:timestamp])/notes([:noteId])` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/goal-notes(preview)/delete-by-id) |
| [Patch By ID](actions/goal-notes-preview-patch-by-id.md) | `PATCH groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/goalValues([:timestamp])/notes([:noteId])` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/goal-notes(preview)/patch-by-id) |
| [Post](actions/goal-notes-preview-post.md) | `POST groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/goalValues([:timestamp])/notes` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/goal-notes(preview)/post) |
| [Delete By ID](actions/goal-values-preview-delete-by-id.md) | `DELETE groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/goalValues([:timestamp])` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/goal-values(preview)/delete-by-id) |
| [Get](actions/goal-values-preview-get.md) | `GET groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/goalValues` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/goal-values(preview)/get) |
| [Get By ID](actions/goal-values-preview-get-by-id.md) | `GET groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/goalValues([:timestamp])` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/goal-values(preview)/get-by-id) |
| [Patch By ID](actions/goal-values-preview-patch-by-id.md) | `PATCH groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/goalValues([:timestamp])` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/goal-values(preview)/patch-by-id) |
| [Post](actions/goal-values-preview-post.md) | `POST groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/goalValues` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/goal-values(preview)/post) |
| [Delete By ID](actions/goals-preview-delete-by-id.md) | `DELETE groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/goals(preview)/delete-by-id) |
| [Delete Goal Current Value Connection](actions/goals-preview-delete-goal-current-value-connection.md) | `POST groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/DeleteGoalCurrentValueConnection()` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/goals(preview)/delete-goal-current-value-connection) |
| [Delete Goal Target Value Connection](actions/goals-preview-delete-goal-target-value-connection.md) | `POST groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/DeleteGoalTargetValueConnection()` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/goals(preview)/delete-goal-target-value-connection) |
| [Get](actions/goals-preview-get.md) | `GET groups/[:groupId]/scorecards([:scorecardId])/goals` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/goals(preview)/get) |
| [Get By ID](actions/goals-preview-get-by-id.md) | `GET groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/goals(preview)/get-by-id) |
| [Get Refresh History](actions/goals-preview-get-refresh-history.md) | `GET groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/GetRefreshHistory()` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/goals(preview)/get-refresh-history) |
| [Patch By ID](actions/goals-preview-patch-by-id.md) | `PATCH groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/goals(preview)/patch-by-id) |
| [Post](actions/goals-preview-post.md) | `POST groups/[:groupId]/scorecards([:scorecardId])/goals` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/goals(preview)/post) |
| [Refresh Goal Current Value](actions/goals-preview-refresh-goal-current-value.md) | `POST groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/RefreshGoalCurrentValue()` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/goals(preview)/refresh-goal-current-value) |
| [Refresh Goal Target Value](actions/goals-preview-refresh-goal-target-value.md) | `POST groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/RefreshGoalTargetValue()` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/goals(preview)/refresh-goal-target-value) |
| [Delete](actions/goals-status-rules-preview-delete.md) | `DELETE groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/statusRules` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/goals-status-rules(preview)/delete) |
| [Get](actions/goals-status-rules-preview-get.md) | `GET groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/statusRules` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/goals-status-rules(preview)/get) |
| [Post](actions/goals-status-rules-preview-post.md) | `POST groups/[:groupId]/scorecards([:scorecardId])/goals([:goalId])/statusRules` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/goals-status-rules(preview)/post) |
| [Import Excel Workbook in Workspace](actions/import-excel-workbook-in-workspace.md) | `POST groups/[:groupId]/imports` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/imports/post-import-in-group) |
| [Create Temporary Upload Location](actions/imports-create-temporary-upload-location.md) | `POST imports/createTemporaryUploadLocation` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/imports/create-temporary-upload-location) |
| [Create Temporary Upload Location In Group](actions/imports-create-temporary-upload-location-in-group.md) | `POST groups/[:groupId]/imports/createTemporaryUploadLocation` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/imports/create-temporary-upload-location-in-group) |
| [Get Import](actions/imports-get-import.md) | `GET imports/[:importId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/imports/get-import) |
| [Get Imports](actions/imports-get-imports.md) | `GET imports` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/imports/get-imports) |
| [Post Import](actions/imports-post-import.md) | `POST imports` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/imports/post-import) |
| [List Dashboard Tiles](actions/list-dashboard-tiles.md) | `GET groups/[:groupId]/dashboards/[:dashboardId]/tiles` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dashboards/get-tiles-in-group) |
| [List Dashboards in Installed App](actions/list-dashboards-in-installed-app.md) | `GET apps/[:appId]/dashboards` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/apps/get-dashboards) |
| [List Dashboards in Workspace](actions/list-dashboards-in-workspace.md) | `GET groups/[:groupId]/dashboards` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dashboards/get-dashboards-in-group) |
| [List Dataflows in Workspace](actions/list-dataflows-in-workspace.md) | `GET groups/[:groupId]/dataflows` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/dataflows/get-dataflows) |
| [List Dataset Datasources](actions/list-dataset-datasources.md) | `GET groups/[:groupId]/datasets/[:datasetId]/datasources` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-datasources-in-group) |
| [List Dataset Refresh History in Workspace](actions/list-dataset-refresh-history-in-workspace.md) | `GET groups/[:groupId]/datasets/[:datasetId]/refreshes` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-refresh-history-in-group) |
| [List Datasets in Workspace](actions/list-datasets-in-workspace.md) | `GET groups/[:groupId]/datasets` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/get-datasets-in-group) |
| [List Imports in Workspace](actions/list-imports-in-workspace.md) | `GET groups/[:groupId]/imports` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/imports/get-imports-in-group) |
| [List Installed Apps](actions/list-installed-apps.md) | `GET apps` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/apps/get-apps) |
| [List Report Pages](actions/list-report-pages.md) | `GET groups/[:groupId]/reports/[:reportId]/pages` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/get-pages-in-group) |
| [List Reports in Installed App](actions/list-reports-in-installed-app.md) | `GET apps/[:appId]/reports` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/apps/get-reports) |
| [List Reports in Workspace](actions/list-reports-in-workspace.md) | `GET groups/[:groupId]/reports` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/get-reports-in-group) |
| [List Workspace Users](actions/list-workspace-users.md) | `GET groups/[:groupId]/users` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/groups/get-group-users) |
| [List Workspaces](actions/list-workspaces.md) | `GET groups` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/groups/get-groups) |
| [Assign Workspace](actions/pipelines-assign-workspace.md) | `POST pipelines/[:pipelineId]/stages/[:stageOrder]/assignWorkspace` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/assign-workspace) |
| [Create Pipeline](actions/pipelines-create-pipeline.md) | `POST pipelines` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/create-pipeline) |
| [Delete Pipeline](actions/pipelines-delete-pipeline.md) | `DELETE pipelines/[:pipelineId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/delete-pipeline) |
| [Delete Pipeline User](actions/pipelines-delete-pipeline-user.md) | `DELETE pipelines/[:pipelineId]/users/[:identifier]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/delete-pipeline-user) |
| [Deploy All](actions/pipelines-deploy-all.md) | `POST pipelines/[:pipelineId]/deployAll` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/deploy-all) |
| [Get Pipeline](actions/pipelines-get-pipeline.md) | `GET pipelines/[:pipelineId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/get-pipeline) |
| [Get Pipeline Operation](actions/pipelines-get-pipeline-operation.md) | `GET pipelines/[:pipelineId]/operations/[:operationId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/get-pipeline-operation) |
| [Get Pipeline Operations](actions/pipelines-get-pipeline-operations.md) | `GET pipelines/[:pipelineId]/operations` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/get-pipeline-operations) |
| [Get Pipeline Stage Artifacts](actions/pipelines-get-pipeline-stage-artifacts.md) | `GET pipelines/[:pipelineId]/stages/[:stageOrder]/artifacts` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/get-pipeline-stage-artifacts) |
| [Get Pipeline Stages](actions/pipelines-get-pipeline-stages.md) | `GET pipelines/[:pipelineId]/stages` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/get-pipeline-stages) |
| [Get Pipeline Users](actions/pipelines-get-pipeline-users.md) | `GET pipelines/[:pipelineId]/users` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/get-pipeline-users) |
| [Get Pipelines](actions/pipelines-get-pipelines.md) | `GET pipelines` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/get-pipelines) |
| [Selective Deploy](actions/pipelines-selective-deploy.md) | `POST pipelines/[:pipelineId]/deploy` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/selective-deploy) |
| [Unassign Workspace](actions/pipelines-unassign-workspace.md) | `POST pipelines/[:pipelineId]/stages/[:stageOrder]/unassignWorkspace` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/unassign-workspace) |
| [Update Pipeline](actions/pipelines-update-pipeline.md) | `PATCH pipelines/[:pipelineId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/update-pipeline) |
| [Update Pipeline User](actions/pipelines-update-pipeline-user.md) | `POST pipelines/[:pipelineId]/users` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/update-pipeline-user) |
| [Create Profile](actions/profiles-create-profile.md) | `POST profiles` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/profiles/create-profile) |
| [Delete Profile](actions/profiles-delete-profile.md) | `DELETE profiles/[:profileId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/profiles/delete-profile) |
| [Get Profile](actions/profiles-get-profile.md) | `GET profiles/[:profileId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/profiles/get-profile) |
| [Get Profiles](actions/profiles-get-profiles.md) | `GET profiles` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/profiles/get-profiles) |
| [Update Profile](actions/profiles-update-profile.md) | `PUT profiles/[:profileId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/profiles/update-profile) |
| [Datasets DeleteRows](actions/push-datasets-datasets-deleterows.md) | `DELETE datasets/[:datasetId]/tables/[:tableName]/rows` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/push-datasets/datasets-delete-rows) |
| [Datasets GetTables](actions/push-datasets-datasets-gettables.md) | `GET datasets/[:datasetId]/tables` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/push-datasets/datasets-get-tables) |
| [Datasets GetTablesInGroup](actions/push-datasets-datasets-gettables-in-group.md) | `GET groups/[:groupId]/datasets/[:datasetId]/tables` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/push-datasets/datasets-get-tables-in-group) |
| [Datasets PostDataset](actions/push-datasets-datasets-postdataset.md) | `POST datasets` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/push-datasets/datasets-post-dataset) |
| [Datasets PostRows](actions/push-datasets-datasets-postrows.md) | `POST datasets/[:datasetId]/tables/[:tableName]/rows` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/push-datasets/datasets-post-rows) |
| [Datasets PutTable](actions/push-datasets-datasets-puttable.md) | `PUT datasets/[:datasetId]/tables/[:tableName]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/push-datasets/datasets-put-table) |
| [Datasets PutTableInGroup](actions/push-datasets-datasets-puttable-in-group.md) | `PUT groups/[:groupId]/datasets/[:datasetId]/tables/[:tableName]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/push-datasets/datasets-put-table-in-group) |
| [Rebind Report in Workspace](actions/rebind-report-in-workspace.md) | `POST groups/[:groupId]/reports/[:reportId]/Rebind` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/rebind-report-in-group) |
| [Refresh Dataset in Workspace](actions/refresh-dataset-in-workspace.md) | `POST groups/[:groupId]/datasets/[:datasetId]/refreshes` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/datasets/refresh-dataset-in-group) |
| [Bind To Gateway](actions/reports-bind-to-gateway.md) | `POST reports/[:reportId]/Default.BindToGateway` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/bind-to-gateway) |
| [Bind To Gateway In Group](actions/reports-bind-to-gateway-in-group.md) | `POST groups/[:groupId]/reports/[:reportId]/Default.BindToGateway` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/bind-to-gateway-in-group) |
| [Clone Report](actions/reports-clone-report.md) | `POST reports/[:reportId]/Clone` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/clone-report) |
| [Delete Report](actions/reports-delete-report.md) | `DELETE reports/[:reportId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/delete-report) |
| [Export Report](actions/reports-export-report.md) | `GET reports/[:reportId]/Export` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/export-report) |
| [Export Report In Group](actions/reports-export-report-in-group.md) | `GET groups/[:groupId]/reports/[:reportId]/Export` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/export-report-in-group) |
| [Export To File](actions/reports-export-to-file.md) | `POST reports/[:reportId]/ExportTo` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/export-to-file) |
| [Export To File In Group](actions/reports-export-to-file-in-group.md) | `POST groups/[:groupId]/reports/[:reportId]/ExportTo` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/export-to-file-in-group) |
| [Get Datasources](actions/reports-get-datasources.md) | `GET reports/[:reportId]/datasources` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/get-datasources) |
| [Get Datasources In Group](actions/reports-get-datasources-in-group.md) | `GET groups/[:groupId]/reports/[:reportId]/datasources` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/get-datasources-in-group) |
| [Get Export To File Status](actions/reports-get-export-to-file-status.md) | `GET reports/[:reportId]/exports/[:exportId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/get-export-to-file-status) |
| [Get Export To File Status In Group](actions/reports-get-export-to-file-status-in-group.md) | `GET groups/[:groupId]/reports/[:reportId]/exports/[:exportId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/get-export-to-file-status-in-group) |
| [Get File Of Export To File](actions/reports-get-file-of-export-to-file.md) | `GET reports/[:reportId]/exports/[:exportId]/file` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/get-file-of-export-to-file) |
| [Get File Of Export To File In Group](actions/reports-get-file-of-export-to-file-in-group.md) | `GET groups/[:groupId]/reports/[:reportId]/exports/[:exportId]/file` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/get-file-of-export-to-file-in-group) |
| [Get Page](actions/reports-get-page.md) | `GET reports/[:reportId]/pages/[:pageName]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/get-page) |
| [Get Pages](actions/reports-get-pages.md) | `GET reports/[:reportId]/pages` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/get-pages) |
| [Get Report](actions/reports-get-report.md) | `GET reports/[:reportId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/get-report) |
| [Get Reports](actions/reports-get-reports.md) | `GET reports` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/get-reports) |
| [Rebind Report](actions/reports-rebind-report.md) | `POST reports/[:reportId]/Rebind` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/rebind-report) |
| [Take Over In Group](actions/reports-take-over-in-group.md) | `POST groups/[:groupId]/reports/[:reportId]/Default.TakeOver` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/take-over-in-group) |
| [Update Datasources](actions/reports-update-datasources.md) | `POST reports/[:reportId]/Default.UpdateDatasources` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/update-datasources) |
| [Update Datasources In Group](actions/reports-update-datasources-in-group.md) | `POST groups/[:groupId]/reports/[:reportId]/Default.UpdateDatasources` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/update-datasources-in-group) |
| [Update Report Content](actions/reports-update-report-content.md) | `POST reports/[:reportId]/UpdateReportContent` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/update-report-content) |
| [Update Report Content In Group](actions/reports-update-report-content-in-group.md) | `POST groups/[:groupId]/reports/[:reportId]/UpdateReportContent` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/update-report-content-in-group) |
| [Delete By ID](actions/scorecards-preview-delete-by-id.md) | `DELETE groups/[:groupId]/scorecards([:scorecardId])` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/scorecards(preview)/delete-by-id) |
| [Get](actions/scorecards-preview-get.md) | `GET groups/[:groupId]/scorecards` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/scorecards(preview)/get) |
| [Get By ID](actions/scorecards-preview-get-by-id.md) | `GET groups/[:groupId]/scorecards([:scorecardId])` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/scorecards(preview)/get-by-id) |
| [Get Scorecard By Report Id](actions/scorecards-preview-get-scorecard-by-report-id.md) | `GET groups/[:groupId]/scorecards/GetScorecardByReportId(reportId=[:reportId])` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/scorecards(preview)/get-scorecard-by-report-id) |
| [Move Goals](actions/scorecards-preview-move-goals.md) | `POST groups/[:groupId]/scorecards([:scorecardId])/MoveGoals()` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/scorecards(preview)/move-goals) |
| [Patch By ID](actions/scorecards-preview-patch-by-id.md) | `PATCH groups/[:groupId]/scorecards([:scorecardId])` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/scorecards(preview)/patch-by-id) |
| [Post](actions/scorecards-preview-post.md) | `POST groups/[:groupId]/scorecards` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/scorecards(preview)/post) |
| [Create Install Ticket](actions/template-apps-create-install-ticket.md) | `POST CreateTemplateAppInstallTicket` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/template-apps/create-install-ticket) |
| [Update Workspace](actions/update-workspace.md) | `PATCH groups/[:groupId]` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/groups/update-group) |
| [Update Workspace User](actions/update-workspace-user.md) | `PUT groups/[:groupId]/users` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/groups/update-group-user) |
| [Refresh User Permissions](actions/users-refresh-user-permissions.md) | `POST RefreshUserPermissions` | [docs](https://learn.microsoft.com/en-us/rest/api/power-bi/users/refresh-user-permissions) |
