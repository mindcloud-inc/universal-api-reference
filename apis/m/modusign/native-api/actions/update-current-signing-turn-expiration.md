# Update Current Signing Turn Expiration with Modusign

Updates the current signing turn expiration in Modusign.

## Endpoint

- **Method:** `PUT`
- **Path:** `/documents/:documentId/change-signing-due`
- **Base URL:** `https://api.modusign.co.kr`
- **Official documentation:** [Update Current Signing Turn Expiration](https://developers.modusign.co.kr/reference/documentcontroller_changesigningdueofcurrentorder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datetime` | body | `string` | yes | The new ISO datetime for the current signing turn expiration. |
| `documentId` | path | `string` | yes | The Modusign document ID. |
