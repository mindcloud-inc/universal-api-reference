# Get Order Log with Cloudprinter.com

Retrieves an order log from Cloudprinter.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/cloudcore/1.0/orders/log`
- **Base URL:** `https://api.cloudprinter.com`
- **Official documentation:** [Get Order Log](https://docs.cloudprinter.com/client/cloudprinter-core-api-v1-0#order-log)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reference` | body | `string` | yes | Client order reference. |
