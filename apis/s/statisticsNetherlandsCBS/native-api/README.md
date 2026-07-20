# Statistics Netherlands CBS: Native API Reference

A consolidated summary of Statistics Netherlands CBS's API configuration and 61 documented operations, with links to official documentation.

- **Official docs:** https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data
- **API base URL:** `https://opendata.cbs.nl`

## Authentication

### No Authentication

CBS StatLine open data endpoints are public and do not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `$top` in the query string to set the page size (default 50; accepted range 1–1000). Use `$skip` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `odataFilter`.

## Sorting

Set the sort field with `$orderby` in the query string. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (61 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Catalog Metadata](actions/get-catalog-metadata.md) | `GET /ODataCatalog/$metadata` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [Get Category Group](actions/get-category-group.md) | `GET /ODataApi/odata/{{tableIdentifier}}/CategoryGroups({{id}})` | [docs](https://www.cbs.nl/en-gb/our-services/open-data/statline-as-open-data/quick-start-guide) |
| [Get Data Property](actions/get-data-property.md) | `GET /ODataApi/odata/{{tableIdentifier}}/DataProperties({{id}})` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [Get Featured Group](actions/get-featured-group.md) | `GET /ODataCatalog/Featured({{id}})` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [Get Feed Category Group](actions/get-feed-category-group.md) | `GET /ODataFeed/odata/{{tableIdentifier}}/CategoryGroups({{id}})` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [Get Feed Data Property](actions/get-feed-data-property.md) | `GET /ODataFeed/odata/{{tableIdentifier}}/DataProperties({{id}})` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [Get Feed Metadata](actions/get-feed-metadata.md) | `GET /ODataFeed/odata/{{tableIdentifier}}/$metadata` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [Get Feed Resource Row](actions/get-feed-resource-row.md) | `GET /ODataFeed/odata/{{tableIdentifier}}/{{resourceName}}('{{key}}')` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [Get Feed Table Info](actions/get-feed-table-info.md) | `GET /ODataFeed/odata/{{tableIdentifier}}/TableInfos({{id}})` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [Get Feed Typed Data Row](actions/get-feed-typed-data-row.md) | `GET /ODataFeed/odata/{{tableIdentifier}}/TypedDataSet({{id}})` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [Get Feed Untyped Data Row](actions/get-feed-untyped-data-row.md) | `GET /ODataFeed/odata/{{tableIdentifier}}/UntypedDataSet({{id}})` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [Get OData V4 Catalog](actions/get-o-data-v4-catalog.md) | `GET https://datasets.cbs.nl/odata/v1/CBS/Catalogs('{{identifier}}')` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [Get OData V4 Dataset](actions/get-o-data-v4-dataset.md) | `GET https://datasets.cbs.nl/odata/v1/CBS/Datasets('{{identifier}}')` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [Get OData V4 Dimension](actions/get-o-data-v4-dimension.md) | `GET https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/Dimensions('{{identifier}}')` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [Get OData V4 Dimension Code](actions/get-o-data-v4-dimension-code.md) | `GET https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/{{dimensionIdentifier}}Codes('{{identifier}}')` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [Get OData V4 Dimension Group](actions/get-o-data-v4-dimension-group.md) | `GET https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/{{dimensionIdentifier}}Groups('{{id}}')` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [Get OData V4 Measure Code](actions/get-o-data-v4-measure-code.md) | `GET https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/MeasureCodes('{{identifier}}')` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [Get OData V4 Measure Group](actions/get-o-data-v4-measure-group.md) | `GET https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/MeasureGroups('{{id}}')` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [Get OData V4 Metadata](actions/get-o-data-v4-metadata.md) | `GET https://datasets.cbs.nl/odata/v1/CBS/$metadata` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [Get OData V4 Observation](actions/get-o-data-v4-observation.md) | `GET https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/Observations({{id}})` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [Get OData V4 Table Metadata](actions/get-o-data-v4-table-metadata.md) | `GET https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/$metadata` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [Get OData V4 Table Properties](actions/get-o-data-v4-table-properties.md) | `GET https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/Properties` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [Get Standard Resource Row](actions/get-standard-resource-row.md) | `GET /ODataApi/odata/{{tableIdentifier}}/{{resourceName}}('{{key}}')` | [docs](https://www.cbs.nl/en-gb/our-services/open-data/statline-as-open-data/quick-start-guide) |
| [Get Table](actions/get-table.md) | `GET /ODataCatalog/Tables({{id}})` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [Get Table Featured Link](actions/get-table-featured-link.md) | `GET /ODataCatalog/Table_Featured({{id}})` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [Get Table Info](actions/get-table-info.md) | `GET /ODataApi/odata/{{tableIdentifier}}/TableInfos({{id}})` | [docs](https://www.cbs.nl/en-gb/our-services/open-data/statline-as-open-data/quick-start-guide) |
| [Get Table Service Metadata](actions/get-table-service-metadata.md) | `GET /ODataApi/odata/{{tableIdentifier}}/$metadata` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [Get Table Theme Link](actions/get-table-theme-link.md) | `GET /ODataCatalog/Tables_Themes({{id}})` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [Get Theme](actions/get-theme.md) | `GET /ODataCatalog/Themes({{id}})` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [Get Typed Data Row](actions/get-typed-data-row.md) | `GET /ODataApi/odata/{{tableIdentifier}}/TypedDataSet({{id}})` | [docs](https://www.cbs.nl/en-gb/our-services/open-data/statline-as-open-data/quick-start-guide) |
| [Get Untyped Data Row](actions/get-untyped-data-row.md) | `GET /ODataApi/odata/{{tableIdentifier}}/UntypedDataSet({{id}})` | [docs](https://www.cbs.nl/en-gb/our-services/open-data/statline-as-open-data/quick-start-guide) |
| [List Catalog Collections](actions/list-catalog-collections.md) | `GET /ODataCatalog` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List Category Groups](actions/list-category-groups.md) | `GET /ODataApi/odata/{{tableIdentifier}}/CategoryGroups` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List Data Properties](actions/list-data-properties.md) | `GET /ODataApi/odata/{{tableIdentifier}}/DataProperties` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List Featured Groups](actions/list-featured-groups.md) | `GET /ODataCatalog/Featured` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List Feed Category Groups](actions/list-feed-category-groups.md) | `GET /ODataFeed/odata/{{tableIdentifier}}/CategoryGroups` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List Feed Data Properties](actions/list-feed-data-properties.md) | `GET /ODataFeed/odata/{{tableIdentifier}}/DataProperties` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List Feed Resource Rows](actions/list-feed-resource-rows.md) | `GET /ODataFeed/odata/{{tableIdentifier}}/{{resourceName}}` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List Feed Service Collections](actions/list-feed-service-collections.md) | `GET /ODataFeed/odata/{{tableIdentifier}}` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List Feed Table Infos](actions/list-feed-table-infos.md) | `GET /ODataFeed/odata/{{tableIdentifier}}/TableInfos` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List Feed Typed Data Rows](actions/list-feed-typed-data-rows.md) | `GET /ODataFeed/odata/{{tableIdentifier}}/TypedDataSet` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List Feed Untyped Data Rows](actions/list-feed-untyped-data-rows.md) | `GET /ODataFeed/odata/{{tableIdentifier}}/UntypedDataSet` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List OData V4 Catalogs](actions/list-o-data-v4-catalogs.md) | `GET https://datasets.cbs.nl/odata/v1/CBS/Catalogs` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List OData V4 Collections](actions/list-o-data-v4-collections.md) | `GET https://datasets.cbs.nl/odata/v1/CBS` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List OData V4 Datasets](actions/list-o-data-v4-datasets.md) | `GET https://datasets.cbs.nl/odata/v1/CBS/Datasets` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List OData V4 Dimension Codes](actions/list-o-data-v4-dimension-codes.md) | `GET https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/{{dimensionIdentifier}}Codes` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List OData V4 Dimension Groups](actions/list-o-data-v4-dimension-groups.md) | `GET https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/{{dimensionIdentifier}}Groups` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List OData V4 Dimensions](actions/list-o-data-v4-dimensions.md) | `GET https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/Dimensions` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List OData V4 Measure Codes](actions/list-o-data-v4-measure-codes.md) | `GET https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/MeasureCodes` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List OData V4 Measure Groups](actions/list-o-data-v4-measure-groups.md) | `GET https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/MeasureGroups` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List OData V4 Observations](actions/list-o-data-v4-observations.md) | `GET https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}/Observations` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List OData V4 Table Collections](actions/list-o-data-v4-table-collections.md) | `GET https://datasets.cbs.nl/odata/v1/CBS/{{tableIdentifier}}` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List Standard Resource Rows](actions/list-standard-resource-rows.md) | `GET /ODataApi/odata/{{tableIdentifier}}/{{resourceName}}` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List Table Featured Links](actions/list-table-featured-links.md) | `GET /ODataCatalog/Table_Featured` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List Table Infos](actions/list-table-infos.md) | `GET /ODataApi/odata/{{tableIdentifier}}/TableInfos` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List Table Service Collections](actions/list-table-service-collections.md) | `GET /ODataApi/odata/{{tableIdentifier}}` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List Table Theme Links](actions/list-table-theme-links.md) | `GET /ODataCatalog/Tables_Themes` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List Tables](actions/list-tables.md) | `GET /ODataCatalog/Tables` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List Themes](actions/list-themes.md) | `GET /ODataCatalog/Themes` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List Typed Data Rows](actions/list-typed-data-rows.md) | `GET /ODataApi/odata/{{tableIdentifier}}/TypedDataSet` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
| [List Untyped Data Rows](actions/list-untyped-data-rows.md) | `GET /ODataApi/odata/{{tableIdentifier}}/UntypedDataSet` | [docs](https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data) |
