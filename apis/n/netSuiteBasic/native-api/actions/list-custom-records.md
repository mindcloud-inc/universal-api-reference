# List Custom Records with NetSuite - Basic

Retrieves a list of custom records from NetSuite.

## Endpoint

- **Method:** `GET`
- **Path:** `/record/v1/:recordType`
- **Base URL:** `https://{accountDomain}.suitetalk.api.netsuite.com/services/rest`
- **Official documentation:** [List Custom Records](https://docs.oracle.com/en/cloud/saas/netsuite/ns-online-help/chapter_1540810168.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recordType` | path | `string` | no | Custom record script ID, such as customrecord_feature. |
