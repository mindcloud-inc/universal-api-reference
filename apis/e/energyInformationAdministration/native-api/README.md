# Energy Information Administration: Native API Reference

A consolidated summary of Energy Information Administration's API configuration and 53 documented operations, with links to official documentation.

- **Official docs:** https://www.eia.gov/opendata/documentation.php
- **OpenAPI specification:** https://www.eia.gov/opendata/eia-api-swagger.zip
- **API base URL:** `https://api.eia.gov/v2`

## Authentication

### API Key

EIA Open Data API key authentication. EIA requires the key as the api_key query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.eia.gov/opendata/documentation.php)

## API conventions

Responses from this API use JSON. Response data is read from `response.data`.

## Pagination

Use `length` in the query string to set the page size (default 25; accepted range 1–5000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sort[0][column]` in the query string. Set the direction separately with `sort[0][direction]`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (53 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Query AEO Data](actions/query-aeo-data.md) | `GET /aeo/{route1}/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query CO2 Emissions Aggregates Data](actions/query-co2-emissions-aggregates-data.md) | `GET /co2-emissions/co2-emissions-aggregates/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query CO2 Emissions And Carbon Coefficients Data](actions/query-co2-emissions-and-carbon-coefficients-data.md) | `GET /co2-emissions/co2-emissions-and-carbon-coefficients/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Coal Aggregate Production Data](actions/query-coal-aggregate-production-data.md) | `GET /coal/aggregate-production/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Coal Consumption And Quality Data](actions/query-coal-consumption-and-quality-data.md) | `GET /coal/consumption-and-quality/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Coal Exports Imports Quantity Price Data](actions/query-coal-exports-imports-quantity-price-data.md) | `GET /coal/exports-imports-quantity-price/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Coal Market Sales Price Data](actions/query-coal-market-sales-price-data.md) | `GET /coal/market-sales-price/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Coal Mine Production Data](actions/query-coal-mine-production-data.md) | `GET /coal/mine-production/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Coal Price By Rank Data](actions/query-coal-price-by-rank-data.md) | `GET /coal/price-by-rank/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Coal Reserves Capacity Data](actions/query-coal-reserves-capacity-data.md) | `GET /coal/reserves-capacity/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Coal Shipments By Mine By Plant Data](actions/query-coal-shipments-by-mine-by-plant-data.md) | `GET /coal/shipments/by-mine-by-plant/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Coal Shipments Mine Aggregates Data](actions/query-coal-shipments-mine-aggregates-data.md) | `GET /coal/shipments/mine-aggregates/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Coal Shipments Mine State Aggregates Data](actions/query-coal-shipments-mine-state-aggregates-data.md) | `GET /coal/shipments/mine-state-aggregates/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Coal Shipments Plant Aggregates Data](actions/query-coal-shipments-plant-aggregates-data.md) | `GET /coal/shipments/plant-aggregates/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Coal Shipments Plant State Aggregates Data](actions/query-coal-shipments-plant-state-aggregates-data.md) | `GET /coal/shipments/plant-state-aggregates/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Coal Shipments Receipts Data](actions/query-coal-shipments-receipts-data.md) | `GET /coal/shipments/receipts/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Crude Oil Imports Data](actions/query-crude-oil-imports-data.md) | `GET /crude-oil-imports/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Densified Biomass Capacity By Region Data](actions/query-densified-biomass-capacity-by-region-data.md) | `GET /densified-biomass/capacity-by-region/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Densified Biomass Characteristics By Region Data](actions/query-densified-biomass-characteristics-by-region-data.md) | `GET /densified-biomass/characteristics-by-region/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Densified Biomass Export Sales And Price Data](actions/query-densified-biomass-export-sales-and-price-data.md) | `GET /densified-biomass/export-sales-and-price/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Densified Biomass Feedstocks And Cost Data](actions/query-densified-biomass-feedstocks-and-cost-data.md) | `GET /densified-biomass/feedstocks-and-cost/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Densified Biomass Inventories By Region Data](actions/query-densified-biomass-inventories-by-region-data.md) | `GET /densified-biomass/inventories-by-region/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Densified Biomass Production By Region Data](actions/query-densified-biomass-production-by-region-data.md) | `GET /densified-biomass/production-by-region/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Densified Biomass Sales And Price By Region Data](actions/query-densified-biomass-sales-and-price-by-region-data.md) | `GET /densified-biomass/sales-and-price-by-region/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Densified Biomass Wood Pellet Plants Data](actions/query-densified-biomass-wood-pellet-plants-data.md) | `GET /densified-biomass/wood-pellet-plants/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Electricity Electric Power Operational Data](actions/query-electricity-electric-power-operational-data.md) | `GET /electricity/electric-power-operational-data/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Electricity Facility Fuel Data](actions/query-electricity-facility-fuel-data.md) | `GET /electricity/facility-fuel/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Electricity Operating Generator Capacity Data](actions/query-electricity-operating-generator-capacity-data.md) | `GET /electricity/operating-generator-capacity/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Electricity Retail Sales Data](actions/query-electricity-retail-sales-data.md) | `GET /electricity/retail-sales/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Electricity RTO Daily Fuel Type Data](actions/query-electricity-rto-daily-fuel-type-data.md) | `GET /electricity/rto/daily-fuel-type-data/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Electricity RTO Daily Interchange Data](actions/query-electricity-rto-daily-interchange-data.md) | `GET /electricity/rto/daily-interchange-data/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Electricity RTO Daily Region Data](actions/query-electricity-rto-daily-region-data.md) | `GET /electricity/rto/daily-region-data/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Electricity RTO Daily Region Sub BA Data](actions/query-electricity-rto-daily-region-sub-ba-data.md) | `GET /electricity/rto/daily-region-sub-ba-data/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Electricity RTO Fuel Type Data](actions/query-electricity-rto-fuel-type-data.md) | `GET /electricity/rto/fuel-type-data/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Electricity RTO Interchange Data](actions/query-electricity-rto-interchange-data.md) | `GET /electricity/rto/interchange-data/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Electricity RTO Region Data](actions/query-electricity-rto-region-data.md) | `GET /electricity/rto/region-data/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Electricity RTO Region Sub BA Data](actions/query-electricity-rto-region-sub-ba-data.md) | `GET /electricity/rto/region-sub-ba-data/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Electricity State Electricity Profiles Capability Data](actions/query-electricity-state-electricity-profiles-capability-data.md) | `GET /electricity/state-electricity-profiles/capability/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Electricity State Electricity Profiles Emissions By State By Fuel Data](actions/query-electricity-state-electricity-profiles-emissions-by-state-by-fuel-data.md) | `GET /electricity/state-electricity-profiles/emissions-by-state-by-fuel/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Electricity State Electricity Profiles Energy Efficiency Data](actions/query-electricity-state-electricity-profiles-energy-efficiency-data.md) | `GET /electricity/state-electricity-profiles/energy-efficiency/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Electricity State Electricity Profiles Meters Data](actions/query-electricity-state-electricity-profiles-meters-data.md) | `GET /electricity/state-electricity-profiles/meters/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Electricity State Electricity Profiles Net Metering Data](actions/query-electricity-state-electricity-profiles-net-metering-data.md) | `GET /electricity/state-electricity-profiles/net-metering/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Electricity State Electricity Profiles Source Disposition Data](actions/query-electricity-state-electricity-profiles-source-disposition-data.md) | `GET /electricity/state-electricity-profiles/source-disposition/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Electricity State Electricity Profiles Summary Data](actions/query-electricity-state-electricity-profiles-summary-data.md) | `GET /electricity/state-electricity-profiles/summary/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query IEO Data](actions/query-ieo-data.md) | `GET /ieo/{route1}/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query International Data](actions/query-international-data.md) | `GET /international/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Natural Gas Data](actions/query-natural-gas-data.md) | `GET /natural-gas/{route1}/{route2}/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Nuclear Outages Facility Nuclear Outages Data](actions/query-nuclear-outages-facility-nuclear-outages-data.md) | `GET /nuclear-outages/facility-nuclear-outages/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Nuclear Outages Generator Nuclear Outages Data](actions/query-nuclear-outages-generator-nuclear-outages-data.md) | `GET /nuclear-outages/generator-nuclear-outages/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Nuclear Outages US Nuclear Outages Data](actions/query-nuclear-outages-us-nuclear-outages-data.md) | `GET /nuclear-outages/us-nuclear-outages/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query SEDS Data](actions/query-seds-data.md) | `GET /seds/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query STEO Data](actions/query-steo-data.md) | `GET /steo/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
| [Query Total Energy Data](actions/query-total-energy-data.md) | `GET /total-energy/data` | [docs](https://www.eia.gov/opendata/documentation.php) |
