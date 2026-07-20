# Download Generated File with Expensify

Retrieves a generated file from Expensify.

## Endpoint

- **Method:** `POST`
- **Path:** `ExpensifyIntegrations`
- **Base URL:** `https://integrations.expensify.com/Integration-Server/`
- **Official documentation:** [Download Generated File](https://integrations.expensify.com/Integration-Server/doc/#downloader)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileName` | body | `string` | yes | The generated file name to download. |
| `fileSystem` | body | `string` | no | integrationServer or reconciliation. Accepted values: `0`, `1`. |
