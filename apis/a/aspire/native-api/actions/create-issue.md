# Create Issue with Aspire

Creates a new issue in your Aspire account.

## Endpoint

- **Method:** `POST`
- **Path:** `Issues`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Create Issue](https://guide.youraspire.com/apidocs/issues-4)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assignedTo` | body | `list<string>` | yes | Send multiple values as a array. |
| `subject` | body | `string` | yes | — |
| `notes` | body | `string` | yes | — |
| `dueDate` | body | `date` | no | — |
| `priority` | body | `string` | no | — |
| `opportunityID` | body | `list<number>` | no | — |
| `propertyID` | body | `list<number>` | no | — |
| `includeClient` | body | `boolean` | no | Format: `toggle`. |
| `publicComment` | body | `boolean` | no | Format: `toggle`. |
| `status` | body | `string` | no | — |
