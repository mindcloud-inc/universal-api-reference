# Create Company with Teamgate

Creates a new company in Teamgate.

## Endpoint

- **Method:** `POST`
- **Path:** `/companies`
- **Base URL:** `https://api.teamgate.com/v4`
- **Official documentation:** [Create Company](https://developers.teamgate.com/#2b3a0450-e365-4f89-b02c-e817d997f627)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Company name. |
| `personId` | body | `string` | no | Existing person ID to associate with the company. |
| `jobTitle` | body | `string` | no | Primary company contact job title. |
| `customerStatusId` | body | `string` | no | Customer status ID. |
| `prospectStatusId` | body | `string` | no | Prospect status ID. |
| `starred` | body | `string` | no | Whether the company is starred. Use Teamgate values like yes or no. |
| `ownerId` | body | `string` | no | Owner user ID. |
| `sourceId` | body | `string` | no | Company source ID. |
| `industryId` | body | `string` | no | Company industry ID. |
| `code` | body | `string` | no | Company registration code. |
| `vatCode` | body | `string` | no | Company VAT code. |
| `tags` | body | `string` | no | Company tags. |
