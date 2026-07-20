# Update Webhook with Anvil

Updates an existing webhook in Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Update Webhook](https://www.useanvil.com/docs/api/graphql/reference/#mutation-updateWebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.eid` | body | `string` | yes | Provide EID for Update Webhook. |
| `variables.url` | body | `string` | no | Provide URL for Update Webhook. |
