# List Record Fields with NetSuite - Basic

Retrieves a list of record fields from NetSuite.

## Endpoint

- **Method:** `GET`
- **Path:** `/record/v1/metadata-catalog/:recordType`
- **Base URL:** `https://{accountDomain}.suitetalk.api.netsuite.com/services/rest`
- **Official documentation:** [List Record Fields](https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/chapter_1540810168.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recordType` | path | `string` | no | NetSuite REST record type ID. |
