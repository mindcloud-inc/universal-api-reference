# Create SFTP Connector with Dromo

Creates a new SFTP connector in Dromo.

## Endpoint

- **Method:** `POST`
- **Path:** `/headless/sftp/connectors/`
- **Base URL:** `https://app.dromo.io/api/v1`
- **Official documentation:** [Create SFTP Connector](https://developer.dromo.io/api-reference/sftp-connectors/create-sftp-connector)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `credentials` | body | `string` | yes | Request body field credentials. |
| `schema` | body | `string` | yes | Request body field schema. |
| `schedule` | body | `object` | yes | Request body field schedule. |
| `directory` | body | `string` | yes | Request body field directory. |
| `file_regex` | body | `string` | no | Request body field file_regex. |
