# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-17-as-10_1776433927596.png" alt="Energy Information Administration logo" width="28" height="28"> Energy Information Administration: Universal API

Access U.S. Energy Information Administration open energy datasets, including electricity, fuel, emissions, forecasts, state energy data, international statistics, and nuclear outage data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/energyInformationAdministration/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 53
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.eia.gov/
- **Vendor API docs:** https://www.eia.gov/opendata/documentation.php

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Query Total Energy Data](actions/query-total-energy-data.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/energyInformationAdministration/latest/actions/query-total-energy-data?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (53)

### Eia Dataset

| Action | Method | Description |
| --- | --- | --- |
| [Query AEO Data](actions/query-aeo-data.md) | GET | Retrieves AEO dataset records from EIA. |
| [Query CO2 Emissions Aggregates Data](actions/query-co2-emissions-aggregates-data.md) | GET | Retrieves CO2 emissions aggregate data from EIA. |
| [Query CO2 Emissions And Carbon Coefficients Data](actions/query-co2-emissions-and-carbon-coefficients-data.md) | GET | Retrieves CO2 emissions and carbon coefficient data from EIA. |
| [Query Coal Aggregate Production Data](actions/query-coal-aggregate-production-data.md) | GET | Retrieves coal aggregate production data from EIA. |
| [Query Coal Consumption And Quality Data](actions/query-coal-consumption-and-quality-data.md) | GET | Retrieves coal consumption and quality data from EIA. |
| [Query Coal Exports Imports Quantity Price Data](actions/query-coal-exports-imports-quantity-price-data.md) | GET | Retrieves coal export and import quantity and price data from EIA. |
| [Query Coal Market Sales Price Data](actions/query-coal-market-sales-price-data.md) | GET | Retrieves coal market sales price data from EIA. |
| [Query Coal Mine Production Data](actions/query-coal-mine-production-data.md) | GET | Retrieves coal mine production data from EIA. |
| [Query Coal Price By Rank Data](actions/query-coal-price-by-rank-data.md) | GET | Retrieves coal price by rank data from EIA. |
| [Query Coal Reserves Capacity Data](actions/query-coal-reserves-capacity-data.md) | GET | Retrieves coal reserves and capacity data from EIA. |
| [Query Coal Shipments By Mine By Plant Data](actions/query-coal-shipments-by-mine-by-plant-data.md) | GET | Retrieves coal shipments by mine and plant data from EIA. |
| [Query Coal Shipments Mine Aggregates Data](actions/query-coal-shipments-mine-aggregates-data.md) | GET | Retrieves coal shipment aggregates by mine from EIA. |
| [Query Coal Shipments Mine State Aggregates Data](actions/query-coal-shipments-mine-state-aggregates-data.md) | GET | Retrieves state coal shipment aggregates by mine from EIA. |
| [Query Coal Shipments Plant Aggregates Data](actions/query-coal-shipments-plant-aggregates-data.md) | GET | Retrieves coal shipment aggregates by plant from EIA. |
| [Query Coal Shipments Plant State Aggregates Data](actions/query-coal-shipments-plant-state-aggregates-data.md) | GET | Retrieves state coal shipment aggregates by plant from EIA. |
| [Query Coal Shipments Receipts Data](actions/query-coal-shipments-receipts-data.md) | GET | Retrieves coal shipment receipts data from EIA. |
| [Query Crude Oil Imports Data](actions/query-crude-oil-imports-data.md) | GET | Retrieves crude oil import data from EIA. |
| [Query Densified Biomass Capacity By Region Data](actions/query-densified-biomass-capacity-by-region-data.md) | GET | Retrieves regional densified biomass capacity data from EIA. |
| [Query Densified Biomass Characteristics By Region Data](actions/query-densified-biomass-characteristics-by-region-data.md) | GET | Retrieves regional densified biomass characteristics data from EIA. |
| [Query Densified Biomass Export Sales And Price Data](actions/query-densified-biomass-export-sales-and-price-data.md) | GET | Retrieves densified biomass export sales and price data from EIA. |
| [Query Densified Biomass Feedstocks And Cost Data](actions/query-densified-biomass-feedstocks-and-cost-data.md) | GET | Retrieves densified biomass feedstock and cost data from EIA. |
| [Query Densified Biomass Inventories By Region Data](actions/query-densified-biomass-inventories-by-region-data.md) | GET | Retrieves regional densified biomass inventory data from EIA. |
| [Query Densified Biomass Production By Region Data](actions/query-densified-biomass-production-by-region-data.md) | GET | Retrieves regional densified biomass production data from EIA. |
| [Query Densified Biomass Sales And Price By Region Data](actions/query-densified-biomass-sales-and-price-by-region-data.md) | GET | Retrieves regional densified biomass sales and price data from EIA. |
| [Query Densified Biomass Wood Pellet Plants Data](actions/query-densified-biomass-wood-pellet-plants-data.md) | GET | Retrieves densified biomass wood pellet plant data from EIA. |
| [Query Electricity Electric Power Operational Data](actions/query-electricity-electric-power-operational-data.md) | GET | Retrieves electric power operational data from EIA. |
| [Query Electricity Facility Fuel Data](actions/query-electricity-facility-fuel-data.md) | GET | Retrieves electricity facility fuel data from EIA. |
| [Query Electricity Operating Generator Capacity Data](actions/query-electricity-operating-generator-capacity-data.md) | GET | Retrieves operating generator capacity data from EIA. |
| [Query Electricity Retail Sales Data](actions/query-electricity-retail-sales-data.md) | GET | Retrieves electricity retail sales data from EIA. |
| [Query Electricity RTO Daily Fuel Type Data](actions/query-electricity-rto-daily-fuel-type-data.md) | GET | Retrieves daily RTO fuel type data from EIA. |
| [Query Electricity RTO Daily Interchange Data](actions/query-electricity-rto-daily-interchange-data.md) | GET | Retrieves daily RTO interchange data from EIA. |
| [Query Electricity RTO Daily Region Data](actions/query-electricity-rto-daily-region-data.md) | GET | Retrieves daily RTO region data from EIA. |
| [Query Electricity RTO Daily Region Sub BA Data](actions/query-electricity-rto-daily-region-sub-ba-data.md) | GET | Retrieves daily RTO region sub-balancing authority data from EIA. |
| [Query Electricity RTO Fuel Type Data](actions/query-electricity-rto-fuel-type-data.md) | GET | Retrieves RTO fuel type data from EIA. |
| [Query Electricity RTO Interchange Data](actions/query-electricity-rto-interchange-data.md) | GET | Retrieves RTO interchange data from EIA. |
| [Query Electricity RTO Region Data](actions/query-electricity-rto-region-data.md) | GET | Retrieves RTO region data from EIA. |
| [Query Electricity RTO Region Sub BA Data](actions/query-electricity-rto-region-sub-ba-data.md) | GET | Retrieves RTO region sub-balancing authority data from EIA. |
| [Query Electricity State Electricity Profiles Capability Data](actions/query-electricity-state-electricity-profiles-capability-data.md) | GET | Retrieves state electricity profile capability data from EIA. |
| [Query Electricity State Electricity Profiles Emissions By State By Fuel Data](actions/query-electricity-state-electricity-profiles-emissions-by-state-by-fuel-data.md) | GET | Retrieves state electricity profile emissions by fuel data from EIA. |
| [Query Electricity State Electricity Profiles Energy Efficiency Data](actions/query-electricity-state-electricity-profiles-energy-efficiency-data.md) | GET | Retrieves state electricity profile energy efficiency data from EIA. |
| [Query Electricity State Electricity Profiles Meters Data](actions/query-electricity-state-electricity-profiles-meters-data.md) | GET | Retrieves state electricity profile meter data from EIA. |
| [Query Electricity State Electricity Profiles Net Metering Data](actions/query-electricity-state-electricity-profiles-net-metering-data.md) | GET | Retrieves state electricity profile net metering data from EIA. |
| [Query Electricity State Electricity Profiles Source Disposition Data](actions/query-electricity-state-electricity-profiles-source-disposition-data.md) | GET | Retrieves state electricity profile source disposition data from EIA. |
| [Query Electricity State Electricity Profiles Summary Data](actions/query-electricity-state-electricity-profiles-summary-data.md) | GET | Retrieves state electricity profile summary data from EIA. |
| [Query IEO Data](actions/query-ieo-data.md) | GET | Retrieves IEO dataset records from EIA. |
| [Query International Data](actions/query-international-data.md) | GET | Retrieves international energy data from EIA. |
| [Query Natural Gas Data](actions/query-natural-gas-data.md) | GET | Retrieves natural gas dataset records from EIA. |
| [Query Nuclear Outages Facility Nuclear Outages Data](actions/query-nuclear-outages-facility-nuclear-outages-data.md) | GET | Retrieves facility nuclear outage data from EIA. |
| [Query Nuclear Outages Generator Nuclear Outages Data](actions/query-nuclear-outages-generator-nuclear-outages-data.md) | GET | Retrieves generator nuclear outage data from EIA. |
| [Query Nuclear Outages US Nuclear Outages Data](actions/query-nuclear-outages-us-nuclear-outages-data.md) | GET | Retrieves U.S. nuclear outage data from EIA. |
| [Query SEDS Data](actions/query-seds-data.md) | GET | Retrieves SEDS dataset records from EIA. |
| [Query STEO Data](actions/query-steo-data.md) | GET | Retrieves STEO dataset records from EIA. |
| [Query Total Energy Data](actions/query-total-energy-data.md) | GET | Retrieves total energy data from EIA. |

