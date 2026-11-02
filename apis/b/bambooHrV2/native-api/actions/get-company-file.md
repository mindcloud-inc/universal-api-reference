# Get Company File with BambooHR

Retrieves company file from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/files/:fileId`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Company File](https://documentation.bamboohr.com/reference/get-company-file)

## Requirements

- **OAuth scopes:** `company_file`
- **scope:** `company_file` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileId` | path | `number` | yes | The ID of the company file to download. |
