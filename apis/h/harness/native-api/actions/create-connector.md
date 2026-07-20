# Create Connector with Harness

Creates a new connector in Harness.

## Endpoint

- **Method:** `POST`
- **Path:** `/ng/api/connectors`
- **Base URL:** `https://app.harness.io/gateway`
- **Official documentation:** [Create Connector](https://apidocs.harness.io/connectors/createconnector)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Connector description. |
| `identifier` | body | `string` | yes | Connector identifier. |
| `name` | body | `string` | yes | Connector display name. |
