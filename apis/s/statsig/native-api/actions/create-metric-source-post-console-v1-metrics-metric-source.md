# Create Metric Source with Statsig

Creates a metric source in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/metrics/metric_source`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Create Metric Source](https://docs.statsig.com/api-reference/metrics/create-metric-source)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Request body field. |
| `description` | body | `string` | no | Request body field. |
| `tags` | body | `list` | no | Request body field. |
| `sql` | body | `string` | yes | Request body field. |
| `timestampColumn` | body | `string` | yes | Request body field. |
| `timestampAsDay` | body | `boolean` | no | Request body field. |
| `idTypeMapping` | body | `list` | yes | Request body field. |
| `sourceType` | body | `string` | no | Request body field. |
| `tableName` | body | `string` | no | Request body field. |
| `datePartitionColumn` | body | `string` | no | Request body field. |
| `customFieldMapping` | body | `list` | no | Request body field. |
| `isReadOnly` | body | `boolean` | no | Request body field. |
| `isVerified` | body | `boolean` | no | Request body field. |
| `disableCURE` | body | `boolean` | no | Request body field. |
| `owner` | body | `object` | no | Request body field. |
| `team` | body | `string` | no | Request body field. |
| `teamID` | body | `string` | no | Request body field. |
| `dryRun` | body | `boolean` | no | Request body field. |
| `skip_validation` | body | `boolean` | no | Request body field. |
| `all_columns` | body | `list` | no | Request body field. |
| `column_types` | body | `list` | no | Request body field. |
