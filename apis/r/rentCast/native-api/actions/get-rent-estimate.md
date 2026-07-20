# Get Rent Estimate with RentCast

Retrieves a rent estimate from RentCast.

## Endpoint

- **Method:** `GET`
- **Path:** `/avm/rent/long-term`
- **Base URL:** `https://api.rentcast.io/v1`
- **Official documentation:** [Get Rent Estimate](https://developers.rentcast.io/reference/rent-estimate-long-term)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | query | `string` | no | The full property address in the format Street, City, State, Zip. |
| `latitude` | query | `number` | no | Latitude of the subject property when using coordinates instead of a full address. |
| `longitude` | query | `number` | no | Longitude of the subject property when using coordinates instead of a full address. |
| `propertyType` | query | `list<string>` | no | The subject property type. Accepted values: `Apartment`, `Condo`, `Manufactured`, `Multi-Family`, `Single Family`, `Townhouse`. |
| `bedrooms` | query | `number` | no | The number of bedrooms in the subject property. |
| `bathrooms` | query | `number` | no | The number of bathrooms in the subject property. |
| `squareFootage` | query | `number` | no | The total living area size of the subject property in square feet. |
| `maxRadius` | query | `number` | no | The maximum distance in miles between comparable listings and the subject property. |
| `daysOld` | query | `number` | no | The maximum number of days since comparable listings were last seen on the market. |
| `compCount` | query | `number` | no | The number of comparable listings to use when calculating the estimate. |
| `lookupSubjectAttributes` | query | `boolean` | no | When enabled, RentCast attempts to look up subject property attributes to find more relevant comps. |
