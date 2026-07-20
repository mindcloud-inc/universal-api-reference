# <img src="https://images.mindcloud.co/apps/icons/starburst-logo-300x470-x_1776801840321.png" alt="Starburst Galaxy logo" width="28" height="28"> Starburst Galaxy: Universal API

Starburst Galaxy is a fully managed data lakehouse and analytics platform built on Trino. This wrapper exposes the Starburst Galaxy Public API for clusters, users, roles, catalogs, tags, service accounts, data products, and data quality summaries.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/starburstGalaxy/latest
- **Category:** Business Intelligence / Data Warehouse
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.starburst.io/starburst-galaxy/
- **Vendor API docs:** https://docs.starburst.io/starburst-galaxy/developer-tools/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List clusters](actions/list-clusters.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/list-clusters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Catalog

| Action | Method | Description |
| --- | --- | --- |
| [Get BigQuery catalog](actions/get-big-query-catalog.md) | GET |  |
| [Get Cassandra catalog](actions/get-cassandra-catalog.md) | GET |  |
| [Get GCS catalog](actions/get-gcs-catalog.md) | GET |  |
| [Get MongoDB catalog](actions/get-mongo-db-catalog.md) | GET |  |
| [Get MySQL catalog](actions/get-my-sql-catalog.md) | GET |  |
| [Get OpenSearch catalog](actions/get-open-search-catalog.md) | GET |  |
| [Get PostgreSQL catalog](actions/get-postgresql-catalog.md) | GET |  |
| [Get Redshift catalog](actions/get-redshift-catalog.md) | GET |  |
| [Get S3 catalog](actions/get-s3-catalog.md) | GET |  |
| [Get Snowflake catalog](actions/get-snowflake-catalog.md) | GET |  |
| [Get SQL Server catalog](actions/get-sql-server-catalog.md) | GET |  |
| [List BigQuery catalogs](actions/list-big-query-catalogs.md) | GET |  |
| [List Cassandra catalogs](actions/list-cassandra-catalogs.md) | GET |  |
| [List catalogs](actions/list-catalogs.md) | GET |  |
| [List GCS catalogs](actions/list-gcs-catalogs.md) | GET |  |
| [List MongoDB catalogs](actions/list-mongo-db-catalogs.md) | GET |  |
| [List MySQL catalogs](actions/list-my-sql-catalogs.md) | GET |  |
| [List OpenSearch catalogs](actions/list-open-search-catalogs.md) | GET |  |
| [List PostgreSQL catalogs](actions/list-postgresql-catalogs.md) | GET |  |
| [List Redshift catalogs](actions/list-redshift-catalogs.md) | GET |  |
| [List S3 catalogs](actions/list-s3-catalogs.md) | GET |  |
| [List Snowflake catalogs](actions/list-snowflake-catalogs.md) | GET |  |
| [List SQL Server catalogs](actions/list-sql-server-catalogs.md) | GET |  |

### Cluster

| Action | Method | Description |
| --- | --- | --- |
| [Get cluster](actions/get-cluster.md) | GET |  |
| [List clusters](actions/list-clusters.md) | GET |  |

### Data Product

| Action | Method | Description |
| --- | --- | --- |
| [Get data product](actions/get-data-product.md) | GET |  |
| [List data products](actions/list-data-products.md) | GET |  |

### Data Quality Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get data quality summary](actions/get-data-quality-summary.md) | GET |  |

### Role

| Action | Method | Description |
| --- | --- | --- |
| [Get role](actions/get-role.md) | GET |  |
| [List roles](actions/list-roles.md) | GET |  |

### Role Grant

| Action | Method | Description |
| --- | --- | --- |
| [List role grants](actions/list-role-grants.md) | GET |  |

### Role Privilege

| Action | Method | Description |
| --- | --- | --- |
| [List role privileges](actions/list-role-privileges.md) | GET |  |

### Schema Discovery

| Action | Method | Description |
| --- | --- | --- |
| [Get schema discovery](actions/get-schema-discovery.md) | GET |  |
| [List catalog schema discoveries](actions/list-catalog-schema-discoveries.md) | GET |  |

### Service Account

| Action | Method | Description |
| --- | --- | --- |
| [Get service account](actions/get-service-account.md) | GET |  |
| [List service accounts](actions/list-service-accounts.md) | GET |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Get tag](actions/get-tag.md) | GET |  |
| [List tags](actions/list-tags.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get user](actions/get-user.md) | GET |  |
| [List users](actions/list-users.md) | GET |  |

