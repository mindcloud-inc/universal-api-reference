# List Products with Logiwa Legacy WMS

## Endpoint

- **Method:** `POST`
- **Path:** `en/api/IntegrationApi/InventoryItemSearch`
- **Base URL:** `https://{uRL}.logiwa.com/`
- **Official documentation:** [List Products](https://developer.logiwa.com/?id=5df0daa0e6466c2eec992f43)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `BarcodeSearch` | body | `string` | no | Barcode of inventory item |
| `Code` | body | `string` | no | Depositor (client) description of inventory item |
| `Description` | body | `string` | no | Description of inventory item |
| `DepositorDescription` | body | `string` | no | Depositor (client) description of inventory item |
| `LastModifiedDate_Start` | body | `date` | no | Last modified date may be filtered within this range - Start |
| `LastModifiedDate_End` | body | `date` | no | Last modified date may be filtered within this range - End |
