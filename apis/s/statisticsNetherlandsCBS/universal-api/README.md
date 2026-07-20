# <img src="https://images.mindcloud.co/apps/icons/statistics-netherlands-cbs-icon_1776711663307.png" alt="Statistics Netherlands CBS logo" width="28" height="28"> Statistics Netherlands CBS: Universal API

Access public Statistics Netherlands (CBS) StatLine open data through the official OData catalog, standard API, and feed services.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/statisticsNetherlandsCBS/latest
- **Actions:** 61
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.cbs.nl/en-gb/our-services/open-data
- **Vendor API docs:** https://www.cbs.nl/en-gb/onze-diensten/open-data/statline-as-open-data

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Catalog Metadata](actions/get-catalog-metadata.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statisticsNetherlandsCBS/latest/actions/get-catalog-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (61)

### Catalog Collection

| Action | Method | Description |
| --- | --- | --- |
| [List Catalog Collections](actions/list-catalog-collections.md) | GET | Retrieves catalog collections from Statistics Netherlands CBS. |

### Catalog Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Catalog Metadata](actions/get-catalog-metadata.md) | GET | Retrieves catalog metadata from Statistics Netherlands CBS. |

### Category Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Category Group](actions/get-category-group.md) | GET | Retrieves a category group from a Statistics Netherlands CBS table. |
| [List Category Groups](actions/list-category-groups.md) | GET | Retrieves category groups from a Statistics Netherlands CBS table. |

### Data Property

| Action | Method | Description |
| --- | --- | --- |
| [Get Data Property](actions/get-data-property.md) | GET | Retrieves a data property from a Statistics Netherlands CBS table. |
| [List Data Properties](actions/list-data-properties.md) | GET | Retrieves data properties from a Statistics Netherlands CBS table. |

### Featured Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Featured Group](actions/get-featured-group.md) | GET | Retrieves a featured group from Statistics Netherlands CBS. |
| [List Featured Groups](actions/list-featured-groups.md) | GET | Retrieves featured groups from Statistics Netherlands CBS. |

### Feed Category Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Feed Category Group](actions/get-feed-category-group.md) | GET | Retrieves a feed category group from a Statistics Netherlands CBS table. |
| [List Feed Category Groups](actions/list-feed-category-groups.md) | GET | Retrieves feed category groups from a Statistics Netherlands CBS table. |

### Feed Data Property

| Action | Method | Description |
| --- | --- | --- |
| [Get Feed Data Property](actions/get-feed-data-property.md) | GET | Retrieves a feed data property from a Statistics Netherlands CBS table. |
| [List Feed Data Properties](actions/list-feed-data-properties.md) | GET | Retrieves feed data properties from a Statistics Netherlands CBS table. |

### Feed Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Feed Metadata](actions/get-feed-metadata.md) | GET | Retrieves feed metadata from a Statistics Netherlands CBS table. |

### Feed Resource Row

| Action | Method | Description |
| --- | --- | --- |
| [Get Feed Resource Row](actions/get-feed-resource-row.md) | GET | Retrieves a feed resource row from a Statistics Netherlands CBS table. |
| [List Feed Resource Rows](actions/list-feed-resource-rows.md) | GET | Retrieves feed resource rows from a Statistics Netherlands CBS table. |

### Feed Service Collection

| Action | Method | Description |
| --- | --- | --- |
| [List Feed Service Collections](actions/list-feed-service-collections.md) | GET | Retrieves feed service collections from a Statistics Netherlands CBS table. |

### Feed Table Info

| Action | Method | Description |
| --- | --- | --- |
| [Get Feed Table Info](actions/get-feed-table-info.md) | GET | Retrieves feed table info from a Statistics Netherlands CBS table. |
| [List Feed Table Infos](actions/list-feed-table-infos.md) | GET | Retrieves feed table info from a Statistics Netherlands CBS table. |

### Feed Typed Data Row

| Action | Method | Description |
| --- | --- | --- |
| [Get Feed Typed Data Row](actions/get-feed-typed-data-row.md) | GET | Retrieves a feed typed data row from a Statistics Netherlands CBS table. |
| [List Feed Typed Data Rows](actions/list-feed-typed-data-rows.md) | GET | Retrieves feed typed data rows from a Statistics Netherlands CBS table. |

### Feed Untyped Data Row

| Action | Method | Description |
| --- | --- | --- |
| [Get Feed Untyped Data Row](actions/get-feed-untyped-data-row.md) | GET | Retrieves a feed untyped data row from a Statistics Netherlands CBS table. |
| [List Feed Untyped Data Rows](actions/list-feed-untyped-data-rows.md) | GET | Retrieves feed untyped data rows from a Statistics Netherlands CBS table. |

### Odata V4 Catalog

| Action | Method | Description |
| --- | --- | --- |
| [Get OData V4 Catalog](actions/get-o-data-v4-catalog.md) | GET | Retrieves an OData V4 catalog from Statistics Netherlands CBS. |
| [List OData V4 Catalogs](actions/list-o-data-v4-catalogs.md) | GET | Retrieves OData V4 catalogs from Statistics Netherlands CBS. |

### Odata V4 Collection

| Action | Method | Description |
| --- | --- | --- |
| [List OData V4 Collections](actions/list-o-data-v4-collections.md) | GET | Retrieves OData V4 collections from Statistics Netherlands CBS. |

### Odata V4 Dataset

| Action | Method | Description |
| --- | --- | --- |
| [Get OData V4 Dataset](actions/get-o-data-v4-dataset.md) | GET | Retrieves an OData V4 dataset from Statistics Netherlands CBS. |
| [List OData V4 Datasets](actions/list-o-data-v4-datasets.md) | GET | Retrieves OData V4 datasets from Statistics Netherlands CBS. |

### Odata V4 Dimension

| Action | Method | Description |
| --- | --- | --- |
| [Get OData V4 Dimension](actions/get-o-data-v4-dimension.md) | GET | Retrieves a dimension from a Statistics Netherlands CBS dataset. |
| [List OData V4 Dimensions](actions/list-o-data-v4-dimensions.md) | GET | Retrieves dimensions from a Statistics Netherlands CBS dataset. |

### Odata V4 Dimension Code

| Action | Method | Description |
| --- | --- | --- |
| [Get OData V4 Dimension Code](actions/get-o-data-v4-dimension-code.md) | GET | Retrieves a dimension code from a Statistics Netherlands CBS dataset. |
| [List OData V4 Dimension Codes](actions/list-o-data-v4-dimension-codes.md) | GET | Retrieves dimension codes from a Statistics Netherlands CBS dataset. |

### Odata V4 Dimension Group

| Action | Method | Description |
| --- | --- | --- |
| [Get OData V4 Dimension Group](actions/get-o-data-v4-dimension-group.md) | GET | Retrieves a dimension group from a Statistics Netherlands CBS dataset. |
| [List OData V4 Dimension Groups](actions/list-o-data-v4-dimension-groups.md) | GET | Retrieves dimension groups from a Statistics Netherlands CBS dataset. |

### Odata V4 Measure Code

| Action | Method | Description |
| --- | --- | --- |
| [Get OData V4 Measure Code](actions/get-o-data-v4-measure-code.md) | GET | Retrieves a measure code from a Statistics Netherlands CBS dataset. |
| [List OData V4 Measure Codes](actions/list-o-data-v4-measure-codes.md) | GET | Retrieves measure codes from a Statistics Netherlands CBS dataset. |

### Odata V4 Measure Group

| Action | Method | Description |
| --- | --- | --- |
| [Get OData V4 Measure Group](actions/get-o-data-v4-measure-group.md) | GET | Retrieves a measure group from a Statistics Netherlands CBS dataset. |
| [List OData V4 Measure Groups](actions/list-o-data-v4-measure-groups.md) | GET | Retrieves measure groups from a Statistics Netherlands CBS dataset. |

### Odata V4 Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get OData V4 Metadata](actions/get-o-data-v4-metadata.md) | GET | Retrieves OData V4 metadata from Statistics Netherlands CBS. |

### Odata V4 Observation

| Action | Method | Description |
| --- | --- | --- |
| [Get OData V4 Observation](actions/get-o-data-v4-observation.md) | GET | Retrieves an observation from a Statistics Netherlands CBS dataset. |
| [List OData V4 Observations](actions/list-o-data-v4-observations.md) | GET | Retrieves observations from a Statistics Netherlands CBS dataset. |

### Odata V4 Table Collection

| Action | Method | Description |
| --- | --- | --- |
| [List OData V4 Table Collections](actions/list-o-data-v4-table-collections.md) | GET | Retrieves OData V4 collections from a Statistics Netherlands CBS dataset. |

### Odata V4 Table Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get OData V4 Table Metadata](actions/get-o-data-v4-table-metadata.md) | GET | Retrieves OData V4 metadata from a Statistics Netherlands CBS dataset. |

### Odata V4 Table Properties

| Action | Method | Description |
| --- | --- | --- |
| [Get OData V4 Table Properties](actions/get-o-data-v4-table-properties.md) | GET | Retrieves table properties from a Statistics Netherlands CBS dataset. |

### Standard Resource Row

| Action | Method | Description |
| --- | --- | --- |
| [Get Standard Resource Row](actions/get-standard-resource-row.md) | GET | Retrieves a standard resource row from a Statistics Netherlands CBS table. |
| [List Standard Resource Rows](actions/list-standard-resource-rows.md) | GET | Retrieves standard resource rows from a Statistics Netherlands CBS table. |

### Table

| Action | Method | Description |
| --- | --- | --- |
| [Get Table](actions/get-table.md) | GET | Retrieves a table from Statistics Netherlands CBS. |
| [List Tables](actions/list-tables.md) | GET | Retrieves tables from Statistics Netherlands CBS. |

### Table Featured Link

| Action | Method | Description |
| --- | --- | --- |
| [Get Table Featured Link](actions/get-table-featured-link.md) | GET | Retrieves a table featured link from Statistics Netherlands CBS. |
| [List Table Featured Links](actions/list-table-featured-links.md) | GET | Retrieves table featured links from Statistics Netherlands CBS. |

### Table Info

| Action | Method | Description |
| --- | --- | --- |
| [Get Table Info](actions/get-table-info.md) | GET | Retrieves table info from a Statistics Netherlands CBS table. |
| [List Table Infos](actions/list-table-infos.md) | GET | Retrieves table info from a Statistics Netherlands CBS table. |

### Table Service Collection

| Action | Method | Description |
| --- | --- | --- |
| [List Table Service Collections](actions/list-table-service-collections.md) | GET | Retrieves service collections from a Statistics Netherlands CBS table. |

### Table Service Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Table Service Metadata](actions/get-table-service-metadata.md) | GET | Retrieves service metadata from a Statistics Netherlands CBS table. |

### Table Theme Link

| Action | Method | Description |
| --- | --- | --- |
| [Get Table Theme Link](actions/get-table-theme-link.md) | GET | Retrieves a table theme link from Statistics Netherlands CBS. |
| [List Table Theme Links](actions/list-table-theme-links.md) | GET | Retrieves table theme links from Statistics Netherlands CBS. |

### Theme

| Action | Method | Description |
| --- | --- | --- |
| [Get Theme](actions/get-theme.md) | GET | Retrieves a theme from Statistics Netherlands CBS. |
| [List Themes](actions/list-themes.md) | GET | Retrieves themes from Statistics Netherlands CBS. |

### Typed Data Row

| Action | Method | Description |
| --- | --- | --- |
| [Get Typed Data Row](actions/get-typed-data-row.md) | GET | Retrieves a typed data row from a Statistics Netherlands CBS table. |
| [List Typed Data Rows](actions/list-typed-data-rows.md) | GET | Retrieves typed data rows from a Statistics Netherlands CBS table. |

### Untyped Data Row

| Action | Method | Description |
| --- | --- | --- |
| [Get Untyped Data Row](actions/get-untyped-data-row.md) | GET | Retrieves an untyped data row from a Statistics Netherlands CBS table. |
| [List Untyped Data Rows](actions/list-untyped-data-rows.md) | GET | Retrieves untyped data rows from a Statistics Netherlands CBS table. |

