# Get Policies with Expensify

Retrieves specific policies from Expensify.

## Endpoint

- **Method:** `POST`
- **Path:** `ExpensifyIntegrations`
- **Base URL:** `https://integrations.expensify.com/Integration-Server/`
- **Official documentation:** [Get Policies](https://integrations.expensify.com/Integration-Server/doc/#policy-getter)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policyIdList` | body | `string` | yes | Comma-separated Expensify policy IDs to fetch. |
| `fields` | body | `string` | yes | Comma-separated policy fields to return: categories, reportFields, tags, tax, employees. |
| `userEmail` | body | `string` | no | Optional user email for third-party accessible domain policy data. |
