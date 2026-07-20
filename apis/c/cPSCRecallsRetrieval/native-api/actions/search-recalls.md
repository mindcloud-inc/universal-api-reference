# Search Recalls with CPSC Recalls Retrieval

Finds public product recalls in CPSC by search fields.

## Endpoint

- **Method:** `GET`
- **Path:** `/Recall`
- **Base URL:** `https://www.saferproducts.gov/RestWebServices`
- **Official documentation:** [Search Recalls](https://www.cpsc.gov/Recalls/CPSC-Recalls-Application-Program-Interface-API-Information?language=en)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `RecallNumber` | query | `string` | no | Find recalls whose recall number matches this value. |
| `RecallTitle` | query | `string` | no | Find recalls whose title contains this text. |
| `RecallDescription` | query | `string` | no | Find recalls whose description contains this text. |
| `ProductName` | query | `string` | no | Find recalls by product name text. |
| `RecallDateStart` | query | `date` | no | Find recalls on or after this recall date. |
| `RecallDateEnd` | query | `date` | no | Find recalls on or before this recall date. |
| `Manufacturer` | query | `string` | no | Find recalls by manufacturer or firm name. |
| `Hazard` | query | `string` | no | Find recalls by hazard text. |
| `Remedy` | query | `string` | no | Find recalls by remedy text. |
| `ConsumerContact` | query | `string` | no | Find recalls whose consumer contact text matches this value. |
| `LastPublishDateStart` | query | `date` | no | Find recalls last published on or after this date. |
| `LastPublishDateEnd` | query | `date` | no | Find recalls last published on or before this date. |
| `RecallURL` | query | `string` | no | Find recalls whose recall URL matches this value. |
| `ProductDescription` | query | `string` | no | Find recalls by product description text. |
| `ProductModel` | query | `string` | no | Find recalls by product model text. |
| `ProductType` | query | `string` | no | Find recalls by product type text. |
| `RecallInconjunctionCountry` | query | `string` | no | Find recalls by country involved in a joint recall. |
| `ImageURL` | query | `string` | no | Find recalls whose image URL matches this value. |
| `Injury` | query | `string` | no | Find recalls by injury text. |
| `ManufacturerCountry` | query | `string` | no | Find recalls by manufacturer country. |
| `UPC` | query | `string` | no | Find recalls by product UPC. |
| `Retailer` | query | `string` | no | Find recalls by retailer text. |
