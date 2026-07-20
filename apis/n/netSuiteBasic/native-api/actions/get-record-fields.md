# Get Record Fields with NetSuite - Basic

Retrieves details for the record fields in NetSuite.

## Endpoint

- **Method:** `GET`
- **Path:** `/record/v1/metadata-catalog/:recordType`
- **Base URL:** `https://{accountDomain}.suitetalk.api.netsuite.com/services/rest`
- **Official documentation:** [Get Record Fields](https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/section_1540810174.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recordType` | path | `string` | no | NetSuite REST record type name. |
