# Get Alert Configuration with BambooHR

Retrieves alert configuration from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/alert-configurations/:id`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Alert Configuration](https://documentation.bamboohr.com/reference/get-alert-configuration)

## Requirements

- **OAuth scopes:** `alerts`
- **scope:** `alerts` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Identifier of the alert configuration to return, as emitted in the `id` field of **List Alert Configurations** (`list-alert-configurations`). This is the configuration's own identifier, not the `bambooAlertId` of the alert template it is based on. No wildcard or `0` sentinel is supported; enumerate configurations with `list-alert-configurations` instead. |
