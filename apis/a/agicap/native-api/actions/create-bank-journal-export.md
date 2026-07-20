# Create Bank Journal Export with Agicap

Creates a bank journal export in Agicap for ready-to-export entries.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/treasury-bank-journal/v1/entities/:entityId/exports/:exportId`
- **Base URL:** `https://api.agicap.com`
- **Official documentation:** [Create Bank Journal Export](https://api.agicap.com/treasury-bank-journal/detailed_documentation.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityId` | path | `string` | yes | Agicap entity identifier. |
| `exportId` | path | `string` | yes | Caller-generated UUID for the export. |
| `currentExportCounts.currentBankJournalsCountInYear` | body | `number` | no | Optional number of bank journals already created this year outside Agicap, for first export numbering continuity. |
| `currentExportCounts.currentBankJournalEntriesCountInYear` | body | `number` | no | Optional number of bank journal entries already created this year outside Agicap, for first export numbering continuity. |
