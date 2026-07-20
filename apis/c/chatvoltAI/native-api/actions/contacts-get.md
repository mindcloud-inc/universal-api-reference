# List Contacts with Chatvolt AI

Retrieves contacts from Chatvolt AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [List Contacts](https://docs.chatvolt.ai/api-reference/endpoint/contacts/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `offset` | query | `number` | no | Number of records to skip for pagination. |
| `limit` | query | `number` | no | Maximum number of records to return. |
| `search` | query | `string` | no | Search term for email, phone number, first name, or last name. |
| `tags[]` | query | `array<string>` | no | List of tags to filter by. |
| `crmScenario` | query | `string` | no | Filter by CRM Scenario ID. |
| `crmStep` | query | `string` | no | Filter by CRM Step ID. |
| `conversationStatus` | query | `string` | no | Filter by conversation status. |
| `agent` | query | `string` | no | Filter by Agent ID. |
| `priority` | query | `string` | no | Filter by conversation priority. |
| `startDate` | query | `string` | no | Filter contacts created on or after this date. |
| `endDate` | query | `string` | no | Filter contacts created on or before this date. |
| `hasEmail` | query | `boolean` | no | Filter contacts that have an email address. |
| `hasPhone` | query | `boolean` | no | Filter contacts that have a phone number. |
| `channel` | query | `string` | no | Filter by conversation channel. |
