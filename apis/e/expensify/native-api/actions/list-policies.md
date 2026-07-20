# List Policies with Expensify

Retrieves policies from Expensify.

## Endpoint

- **Method:** `POST`
- **Path:** `ExpensifyIntegrations`
- **Base URL:** `https://integrations.expensify.com/Integration-Server/`
- **Official documentation:** [List Policies](https://integrations.expensify.com/Integration-Server/doc/#policy-list-getter)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `adminOnly` | body | `boolean` | no | Whether to return only policies where the selected user is an admin. |
| `userEmail` | body | `string` | no | Optional user email to gather the policy list for when third-party domain access has been granted. |
