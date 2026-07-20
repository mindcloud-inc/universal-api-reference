# Update Integration Config with Port API AI

Updates integration configuration in Port.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/integration/:identifier/config`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Update Integration Config](https://docs.port.io/api-reference/update-an-integrations-config)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | The integration identifier. |
| `config` | body | `object` | yes | Integration configuration payload. |
