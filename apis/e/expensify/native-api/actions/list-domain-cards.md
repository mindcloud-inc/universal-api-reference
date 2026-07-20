# List Domain Cards with Expensify

Retrieves domain cards from Expensify.

## Endpoint

- **Method:** `POST`
- **Path:** `ExpensifyIntegrations`
- **Base URL:** `https://integrations.expensify.com/Integration-Server/`
- **Official documentation:** [List Domain Cards](https://integrations.expensify.com/Integration-Server/doc/#domain-cards-getter)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | The domain to list assigned cards for. |
