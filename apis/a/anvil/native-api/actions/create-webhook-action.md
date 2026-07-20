# Create Webhook Action with Anvil

Creates a new webhook action in Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Create Webhook Action](https://www.useanvil.com/docs/api/graphql/reference/#mutation-createWebhookAction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.action` | body | `string` | yes | Provide Action for Create Webhook Action. |
| `variables.objectType` | body | `string` | yes | Provide Object Type for Create Webhook Action. |
| `variables.objectEid` | body | `string` | yes | Provide Object EID for Create Webhook Action. |
| `variables.config` | body | `object` | no | Provide Config for Create Webhook Action. |
| `variables.webhookEid` | body | `string` | no | Provide Webhook EID for Create Webhook Action. |
| `variables.organizationEid` | body | `string` | no | Provide Organization EID for Create Webhook Action. |
| `variables.url` | body | `string` | no | Provide URL for Create Webhook Action. |
