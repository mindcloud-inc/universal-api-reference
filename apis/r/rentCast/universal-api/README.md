# <img src="https://images.mindcloud.co/apps/icons/rent-cast_1774025993800.png" alt="RentCast logo" width="28" height="28"> RentCast: Universal API

Search property records, valuations, listings, and market statistics

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rentCast/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://rentcast.io
- **Vendor API docs:** https://developers.rentcast.io/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Random Property Records](actions/list-random-property-records.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rentCast/latest/actions/list-random-property-records?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Market Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Market Statistics](actions/get-market-statistics.md) | GET | Retrieves market statistics from RentCast for a ZIP code. |

### Property Record

| Action | Method | Description |
| --- | --- | --- |
| [Get Property Record by ID](actions/get-property-record-by-id.md) | GET | Retrieves a property record from RentCast by ID. |
| [List Random Property Records](actions/list-random-property-records.md) | GET | Retrieves random property records from RentCast. |
| [Search Property Records](actions/search-property-records.md) | GET | Finds property records in RentCast by address or area. |

### Rent Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Get Rent Estimate](actions/get-rent-estimate.md) | GET | Retrieves a rent estimate from RentCast. |

### Rental Listing

| Action | Method | Description |
| --- | --- | --- |
| [Get Rental Listing by ID](actions/get-rental-listing-by-id.md) | GET | Retrieves a rental listing from RentCast by ID. |
| [Search Rental Listings](actions/search-rental-listings.md) | GET | Finds rental listings in RentCast by address or area. |

### Sale Listing

| Action | Method | Description |
| --- | --- | --- |
| [Get Sale Listing by ID](actions/get-sale-listing-by-id.md) | GET | Retrieves a sale listing from RentCast by ID. |
| [Search Sale Listings](actions/search-sale-listings.md) | GET | Finds sale listings in RentCast by address or area. |

### Value Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Get Value Estimate](actions/get-value-estimate.md) | GET | Retrieves a property value estimate from RentCast. |

