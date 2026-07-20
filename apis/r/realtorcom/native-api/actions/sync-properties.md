# Sync Properties with Realtor.com

## Endpoint

- **Method:** `GET`
- **Path:** `/odata/Sync`
- **Base URL:** `https://api.listhub.com`
- **Official documentation:** [Sync Properties](https://www.listhub.com/api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | Optional OData filter expression. ListHub recommends Sync for ListingKey and ModificationTimestamp comparison. |
