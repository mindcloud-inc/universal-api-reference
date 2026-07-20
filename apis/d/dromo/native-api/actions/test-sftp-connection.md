# Test SFTP Connection with Dromo

Tests an SFTP credential connection in Dromo.

## Endpoint

- **Method:** `POST`
- **Path:** `/headless/sftp/credentials/:id/test_connection/`
- **Base URL:** `https://app.dromo.io/api/v1`
- **Official documentation:** [Test SFTP Connection](https://developer.dromo.io/api-reference/sftp-credentials/test-sftp-connection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Path parameter id. |
