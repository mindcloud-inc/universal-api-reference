# Start Pipeline Update with Databricks

Starts a pipeline update in Databricks.

## Endpoint

- **Method:** `POST`
- **Path:** `{host}/api/2.0/pipelines/:pipelineId/updates`
- **Base URL:** `https://accounts.cloud.databricks.com`
- **Official documentation:** [Start Pipeline Update](https://docs.databricks.com/api/workspace/pipelines/startupdate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipeline_id` | path | `string` | yes | — |
| `cause` | body | `string` | no | What triggered this update. |
| `full_refresh` | body | `boolean` | no | If true, this update will reset all tables before running. |
| `full_refresh_selection` | body | `list<string>` | yes | A list of tables to update with fullRefresh. If both refresh_selection and full_refresh_selection are empty, this is a full graph update. Full Refresh on a table means that the states of the table will be reset before the refresh. |
| `refresh_selection` | body | `list<string>` | yes | A list of tables to update without fullRefresh. If both refresh_selection and full_refresh_selection are empty, this is a full graph update. Full Refresh on a table means that the states of the table will be reset before the refresh. |
| `reset_checkpoint_selection` | body | `list<string>` | yes | A list of flows for which this update should reset the streaming checkpoint. This selection will not clear the data in the flow's target table. Flows in this list may also appear in refresh_selection and full_refresh_selection. |
| `validate_only` | body | `boolean` | no | If true, this update only validates the correctness of pipeline source code but does not materialize or publish any datasets. |
