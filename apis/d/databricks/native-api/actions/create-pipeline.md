# Create Pipeline with Databricks

Creates a new pipeline in the Databricks workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `{host}/api/2.0/pipelines`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [Create Pipeline](https://docs.databricks.com/api/workspace/pipelines/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `allow_duplicate_names` | body | `boolean` | no | If false, deployment will fail if name conflicts with that of another pipeline. |
| `budget_policy_id` | body | `string` | no | Budget policy of this pipeline. |
| `catalog` | body | `string` | no | A catalog in Unity Catalog to publish data from this pipeline to. If `target` is specified, tables in this pipeline are published to a `target` schema inside `catalog` (for example, `catalog`.`target`.`table`). If `target` is not specified, no data is published to Unity Catalog. |
| `channel` | body | `string` | no | DLT Release Channel that specifies which version to use. |
| `clusters` | body | `list<string>` | yes | Cluster settings for this pipeline deployment. |
| `configuration` | body | `object` | no | String-String configuration for this pipeline execution. |
| `continuous` | body | `boolean` | no | Whether the pipeline is continuous or triggered. This replaces `trigger`. |
| `deployment` | body | `object` | no | — |
| `deployment.kind` | body | `string` | yes | The deployment method that manages the pipeline: - BUNDLE: The pipeline is managed by a Databricks Asset Bundle. |
| `metadata_file_path` | body | `string` | no | The path to the file containing metadata about the deployment. |
| `development` | body | `boolean` | no | Whether the pipeline is in Development mode. Defaults to false. |
| `dry_run` | body | `boolean` | no | — |
| `edition` | body | `string` | no | Pipeline product edition. |
| `environment` | body | `object` | no | The environment entity used to preserve serverless environment side panel, jobs' environment for non-notebook task, and DLT's environment for classic and serverless pipelines. In this minimal environment spec, only pip dependencies are supported. |
| `environment.dependencies` | body | `list<string>` | no | List of pip dependencies, as supported by the version of pip in this environment. Each dependency is a pip requirement file line https://pip.pypa.io/en/stable/reference/requirements-file-format/ Allowed dependency could be <requirement specifier>, <archive url/path>, <local project path>(WSFS or Volumes in Databricks), <vcs project url> |
| `event_log` | body | `object` | no | Configurable event log parameters. |
| `eventLog.catalog` | body | `string` | no | The UC catalog the event log is published under. |
| `eventLog.name` | body | `string` | no | The name the event log is published to in UC. |
| `eventLog.schema` | body | `string` | no | The UC schema the event log is published under. |
| `filters` | body | `object` | no | — |
| `filters.exclude` | body | `list<string>` | no | Paths to exclude. |
| `filters.include` | body | `list<string>` | no | Paths to include. |
| `id` | body | `string` | no | Unique identifier for this pipeline. |
| `ingestion_definition` | body | `object` | no | — |
| `connection_name` | body | `string` | no | The Unity Catalog connection that this ingestion pipeline uses to communicate with the source. This is used with both connectors for applications like Salesforce, Workday, and so on, and also database connectors like Oracle, (connector_type = QUERY_BASED OR connector_type = CDC). If connection name corresponds to database connectors like Oracle, and connector_type is not provided then connector_type defaults to QUERY_BASED. If connector_type is passed as CDC we use Combined Cdc Managed Ingestion pipeline. Under certain conditions, this can be replaced with ingestion_gateway_id to change the connector to Cdc Managed Ingestion Pipeline with Gateway pipeline. |
| `full_refresh_window` | body | `object` | no | Proto representing a window |
| `ingestion_gateway_id` | body | `string` | no | Identifier for the gateway that is used by this ingestion pipeline to communicate with the source database. This is used with CDC connectors to databases like SQL Server using a gateway pipeline (connector_type = CDC). Under certain conditions, this can be replaced with connection_name to change the connector to Combined Cdc Managed Ingestion Pipeline. |
| `ingestionDefinition.objects` | body | `list<string>` | no | Required. Settings specifying tables to replicate and the destination for the replicated tables. |
| `source_configurations` | body | `list<string>` | no | Top-level source configurations |
| `source_type` | body | `string` | no | — |
| `table_configuration` | body | `object` | no | — |
| `libraries` | body | `list<string>` | yes | Libraries or code needed by this deployment. |
| `name` | body | `string` | no | Friendly identifier for this pipeline. |
| `notifications` | body | `list<string>` | yes | List of notification settings for this pipeline. |
| `photon` | body | `boolean` | no | Whether Photon is enabled for this pipeline. |
| `root_path` | body | `string` | no | Root path for this pipeline. This is used as the root directory when editing the pipeline in the Databricks user interface and it is added to sys.path when executing Python sources during pipeline execution. |
| `run_as` | body | `object` | no | Write-only setting, available only in Create/Update calls. Specifies the user or service principal that the pipeline runs as. If not specified, the pipeline runs as the user who created the pipeline.  Only `user_name` or `service_principal_name` can be specified. If both are specified, an error is thrown. |
| `service_principal_name` | body | `string` | no | Application ID of an active service principal. Setting this field requires the `servicePrincipal/user` role. |
| `user_name` | body | `string` | no | The email of an active workspace user. Users can only set this field to their own email. |
| `schema` | body | `string` | no | The default schema (database) where tables are read from or published to. |
| `serverless` | body | `boolean` | no | Whether serverless compute is enabled for this pipeline. |
| `storage` | body | `string` | no | DBFS root directory for storing checkpoints and tables. |
| `tags` | body | `object` | no | A map of tags associated with the pipeline. These are forwarded to the cluster as cluster tags, and are therefore subject to the same limitations. A maximum of 25 tags can be added to the pipeline. |
| `target` | body | `string` | no | Target schema (database) to add tables in this pipeline to. Exactly one of `schema` or `target` must be specified. To publish to Unity Catalog, also specify `catalog`. This legacy field is deprecated for pipeline creation in favor of the `schema` field. |
| `trigger` | body | `object` | no | — |
| `trigger.cron` | body | `object` | no | — |
| `trigger.manual` | body | `object` | no | — |
