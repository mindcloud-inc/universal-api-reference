# Create Webhook with Anvil

Creates a new webhook in Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Create Webhook](https://www.useanvil.com/docs/api/graphql/reference/#mutation-createWebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.organizationEid` | body | `string` | no | Provide Organization EID for Create Webhook. |
| `variables.organizationSlug` | body | `string` | no | Provide Organization Slug for Create Webhook. |
| `variables.url` | body | `string` | no | Provide URL for Create Webhook. |
