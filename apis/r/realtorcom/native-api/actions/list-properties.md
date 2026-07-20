# List Properties with Realtor.com

## Endpoint

- **Method:** `GET`
- **Path:** `/odata/Property`
- **Base URL:** `https://api.listhub.com`
- **Official documentation:** [List Properties](https://www.listhub.com/api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | Optional OData filter expression. ListHub documents supported fields including PropertyType, ListingId, ModificationTimestamp, StandardStatus, SourceSystemID, PostalCode, Country, ListingKey, ListPrice, PropertySubType, StateOrProvince, and TransactionType. |
| `$select` | query | `string` | no | Comma-separated RESO field names to return, for example ListingKey,StandardStatus,ListPrice. |
| `$orderby` | query | `string` | no | Optional OData order expression. ListHub documents ordering on ListingKey and ModificationTimestamp only. |
| `$count` | query | `boolean` | no | Set true to request an @odata.count value when supported for the query. |
