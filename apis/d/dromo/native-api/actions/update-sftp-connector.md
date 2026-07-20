# Update SFTP Connector with Dromo

Updates an existing SFTP connector in Dromo.

## Endpoint

- **Method:** `PUT`
- **Path:** `/headless/sftp/connectors/:id/`
- **Base URL:** `https://app.dromo.io/api/v1`
- **Official documentation:** [Update SFTP Connector](https://developer.dromo.io/api-reference/sftp-connectors/update-sftp-connector)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Path parameter id. |
| `credentials` | body | `string` | yes | Request body field credentials. |
| `schema` | body | `string` | yes | Request body field schema. |
| `schedule` | body | `object` | yes | Request body field schedule. |
| `directory` | body | `string` | yes | Request body field directory. |
| `file_regex` | body | `string` | no | Request body field file_regex. |
