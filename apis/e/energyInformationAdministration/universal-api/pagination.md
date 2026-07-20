# Energy Information Administration Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Energy Information Administration expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/energyInformationAdministration/latest/actions/query-aeo-data?connectionId=$CONNECTION_ID&limit=25&offset=0&route1=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Energy Information Administration actions that support pagination

- [Query AEO Data](actions/query-aeo-data.md)
- [Query CO2 Emissions Aggregates Data](actions/query-co2-emissions-aggregates-data.md)
- [Query CO2 Emissions And Carbon Coefficients Data](actions/query-co2-emissions-and-carbon-coefficients-data.md)
- [Query Coal Aggregate Production Data](actions/query-coal-aggregate-production-data.md)
- [Query Coal Consumption And Quality Data](actions/query-coal-consumption-and-quality-data.md)
- [Query Coal Exports Imports Quantity Price Data](actions/query-coal-exports-imports-quantity-price-data.md)
- [Query Coal Market Sales Price Data](actions/query-coal-market-sales-price-data.md)
- [Query Coal Mine Production Data](actions/query-coal-mine-production-data.md)
- [Query Coal Price By Rank Data](actions/query-coal-price-by-rank-data.md)
- [Query Coal Reserves Capacity Data](actions/query-coal-reserves-capacity-data.md)
- [Query Coal Shipments By Mine By Plant Data](actions/query-coal-shipments-by-mine-by-plant-data.md)
- [Query Coal Shipments Mine Aggregates Data](actions/query-coal-shipments-mine-aggregates-data.md)
- [Query Coal Shipments Mine State Aggregates Data](actions/query-coal-shipments-mine-state-aggregates-data.md)
- [Query Coal Shipments Plant Aggregates Data](actions/query-coal-shipments-plant-aggregates-data.md)
- [Query Coal Shipments Plant State Aggregates Data](actions/query-coal-shipments-plant-state-aggregates-data.md)
- [Query Coal Shipments Receipts Data](actions/query-coal-shipments-receipts-data.md)
- [Query Crude Oil Imports Data](actions/query-crude-oil-imports-data.md)
- [Query Densified Biomass Capacity By Region Data](actions/query-densified-biomass-capacity-by-region-data.md)
- [Query Densified Biomass Characteristics By Region Data](actions/query-densified-biomass-characteristics-by-region-data.md)
- [Query Densified Biomass Export Sales And Price Data](actions/query-densified-biomass-export-sales-and-price-data.md)
- [Query Densified Biomass Feedstocks And Cost Data](actions/query-densified-biomass-feedstocks-and-cost-data.md)
- [Query Densified Biomass Inventories By Region Data](actions/query-densified-biomass-inventories-by-region-data.md)
- [Query Densified Biomass Production By Region Data](actions/query-densified-biomass-production-by-region-data.md)
- [Query Densified Biomass Sales And Price By Region Data](actions/query-densified-biomass-sales-and-price-by-region-data.md)
- [Query Densified Biomass Wood Pellet Plants Data](actions/query-densified-biomass-wood-pellet-plants-data.md)
- [Query Electricity Electric Power Operational Data](actions/query-electricity-electric-power-operational-data.md)
- [Query Electricity Facility Fuel Data](actions/query-electricity-facility-fuel-data.md)
- [Query Electricity Operating Generator Capacity Data](actions/query-electricity-operating-generator-capacity-data.md)
- [Query Electricity Retail Sales Data](actions/query-electricity-retail-sales-data.md)
- [Query Electricity RTO Daily Fuel Type Data](actions/query-electricity-rto-daily-fuel-type-data.md)
- [Query Electricity RTO Daily Interchange Data](actions/query-electricity-rto-daily-interchange-data.md)
- [Query Electricity RTO Daily Region Data](actions/query-electricity-rto-daily-region-data.md)
- [Query Electricity RTO Daily Region Sub BA Data](actions/query-electricity-rto-daily-region-sub-ba-data.md)
- [Query Electricity RTO Fuel Type Data](actions/query-electricity-rto-fuel-type-data.md)
- [Query Electricity RTO Interchange Data](actions/query-electricity-rto-interchange-data.md)
- [Query Electricity RTO Region Data](actions/query-electricity-rto-region-data.md)
- [Query Electricity RTO Region Sub BA Data](actions/query-electricity-rto-region-sub-ba-data.md)
- [Query Electricity State Electricity Profiles Capability Data](actions/query-electricity-state-electricity-profiles-capability-data.md)
- [Query Electricity State Electricity Profiles Emissions By State By Fuel Data](actions/query-electricity-state-electricity-profiles-emissions-by-state-by-fuel-data.md)
- [Query Electricity State Electricity Profiles Energy Efficiency Data](actions/query-electricity-state-electricity-profiles-energy-efficiency-data.md)
- [Query Electricity State Electricity Profiles Meters Data](actions/query-electricity-state-electricity-profiles-meters-data.md)
- [Query Electricity State Electricity Profiles Net Metering Data](actions/query-electricity-state-electricity-profiles-net-metering-data.md)
- [Query Electricity State Electricity Profiles Source Disposition Data](actions/query-electricity-state-electricity-profiles-source-disposition-data.md)
- [Query Electricity State Electricity Profiles Summary Data](actions/query-electricity-state-electricity-profiles-summary-data.md)
- [Query IEO Data](actions/query-ieo-data.md)
- [Query International Data](actions/query-international-data.md)
- [Query Natural Gas Data](actions/query-natural-gas-data.md)
- [Query Nuclear Outages Facility Nuclear Outages Data](actions/query-nuclear-outages-facility-nuclear-outages-data.md)
- [Query Nuclear Outages Generator Nuclear Outages Data](actions/query-nuclear-outages-generator-nuclear-outages-data.md)
- [Query Nuclear Outages US Nuclear Outages Data](actions/query-nuclear-outages-us-nuclear-outages-data.md)
- [Query SEDS Data](actions/query-seds-data.md)
- [Query STEO Data](actions/query-steo-data.md)
- [Query Total Energy Data](actions/query-total-energy-data.md)
