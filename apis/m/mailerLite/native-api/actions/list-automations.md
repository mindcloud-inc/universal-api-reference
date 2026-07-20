# List Automations with MailerLite

Retrieves a page of automations from MailerLite.

## Endpoint

- **Method:** `GET`
- **Path:** `/automations`
- **Base URL:** `https://connect.mailerlite.com/api`
- **Official documentation:** [List Automations](https://developers.mailerlite.com/docs/automations#list-all-automations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[enabled]` | query | `boolean` | no | Return active automations when true and inactive automations when false. |
| `filter[name]` | query | `string` | no | Filter automations by name. |
| `filter[group]` | query | `string` | no | Filter automations by trigger group ID. |
| `limit` | query | `number` | no | Number of automations to return per page. |
| `page` | query | `number` | no | Page number to return. |
