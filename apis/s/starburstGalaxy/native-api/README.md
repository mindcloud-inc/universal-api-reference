# Starburst Galaxy: Native API Reference

A consolidated summary of Starburst Galaxy's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.starburst.io/starburst-galaxy/developer-tools/api/
- **OpenAPI specification:** https://galaxy.starburst.io/public/openapi/v1/json
- **API base URL:** `https://mindcloud.galaxy.starburst.io`

## Authentication

### OAuth2 client credentials

Starburst Galaxy API authentication token using OAuth2 client credentials.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://mindcloud.galaxy.starburst.io/oauth/v2/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.starburst.io/starburst-galaxy/developer-tools/api/api-auth-token.html)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get BigQuery catalog](actions/get-big-query-catalog.md) | `GET /public/api/v1/catalogType/bigquery/catalog/{catalogId}` | [docs](https://galaxy.starburst.io/public-api) |
| [Get Cassandra catalog](actions/get-cassandra-catalog.md) | `GET /public/api/v1/catalogType/cassandra/catalog/{catalogId}` | [docs](https://galaxy.starburst.io/public-api) |
| [Get cluster](actions/get-cluster.md) | `GET /public/api/v1/cluster/{clusterId}` | [docs](https://galaxy.starburst.io/public-api) |
| [Get data product](actions/get-data-product.md) | `GET /public/api/v1/dataProduct/{dataProductId}` | [docs](https://galaxy.starburst.io/public-api) |
| [Get data quality summary](actions/get-data-quality-summary.md) | `GET /public/api/v1/dataQualitySummary` | [docs](https://galaxy.starburst.io/public-api) |
| [Get GCS catalog](actions/get-gcs-catalog.md) | `GET /public/api/v1/catalogType/gcs/catalog/{catalogId}` | [docs](https://galaxy.starburst.io/public-api) |
| [Get MongoDB catalog](actions/get-mongo-db-catalog.md) | `GET /public/api/v1/catalogType/mongodb/catalog/{catalogId}` | [docs](https://galaxy.starburst.io/public-api) |
| [Get MySQL catalog](actions/get-my-sql-catalog.md) | `GET /public/api/v1/catalogType/mysql/catalog/{catalogId}` | [docs](https://galaxy.starburst.io/public-api) |
| [Get OpenSearch catalog](actions/get-open-search-catalog.md) | `GET /public/api/v1/catalogType/opensearch/catalog/{catalogId}` | [docs](https://galaxy.starburst.io/public-api) |
| [Get PostgreSQL catalog](actions/get-postgresql-catalog.md) | `GET /public/api/v1/catalogType/postgresql/catalog/{catalogId}` | [docs](https://galaxy.starburst.io/public-api) |
| [Get Redshift catalog](actions/get-redshift-catalog.md) | `GET /public/api/v1/catalogType/redshift/catalog/{catalogId}` | [docs](https://galaxy.starburst.io/public-api) |
| [Get role](actions/get-role.md) | `GET /public/api/v1/role/{roleId}` | [docs](https://galaxy.starburst.io/public-api) |
| [Get S3 catalog](actions/get-s3-catalog.md) | `GET /public/api/v1/catalogType/s3/catalog/{catalogId}` | [docs](https://galaxy.starburst.io/public-api) |
| [Get schema discovery](actions/get-schema-discovery.md) | `GET /public/api/v1/schemaDiscovery/{schemaDiscoveryId}` | [docs](https://galaxy.starburst.io/public-api) |
| [Get service account](actions/get-service-account.md) | `GET /public/api/v1/serviceAccount/{serviceAccountId}` | [docs](https://galaxy.starburst.io/public-api) |
| [Get Snowflake catalog](actions/get-snowflake-catalog.md) | `GET /public/api/v1/catalogType/snowflake/catalog/{catalogId}` | [docs](https://galaxy.starburst.io/public-api) |
| [Get SQL Server catalog](actions/get-sql-server-catalog.md) | `GET /public/api/v1/catalogType/sqlserver/catalog/{catalogId}` | [docs](https://galaxy.starburst.io/public-api) |
| [Get tag](actions/get-tag.md) | `GET /public/api/v1/tag/{tagId}` | [docs](https://galaxy.starburst.io/public-api) |
| [Get user](actions/get-user.md) | `GET /public/api/v1/user/{userId}` | [docs](https://galaxy.starburst.io/public-api) |
| [List BigQuery catalogs](actions/list-big-query-catalogs.md) | `GET /public/api/v1/catalogType/bigquery/catalog` | [docs](https://galaxy.starburst.io/public-api) |
| [List Cassandra catalogs](actions/list-cassandra-catalogs.md) | `GET /public/api/v1/catalogType/cassandra/catalog` | [docs](https://galaxy.starburst.io/public-api) |
| [List catalog schema discoveries](actions/list-catalog-schema-discoveries.md) | `GET /public/api/v1/catalog/{catalogId}/schemaDiscovery` | [docs](https://galaxy.starburst.io/public-api) |
| [List catalogs](actions/list-catalogs.md) | `GET /public/api/v1/catalog` | [docs](https://galaxy.starburst.io/public-api) |
| [List clusters](actions/list-clusters.md) | `GET /public/api/v1/cluster` | [docs](https://galaxy.starburst.io/public-api) |
| [List data products](actions/list-data-products.md) | `GET /public/api/v1/dataProduct` | [docs](https://galaxy.starburst.io/public-api) |
| [List GCS catalogs](actions/list-gcs-catalogs.md) | `GET /public/api/v1/catalogType/gcs/catalog` | [docs](https://galaxy.starburst.io/public-api) |
| [List MongoDB catalogs](actions/list-mongo-db-catalogs.md) | `GET /public/api/v1/catalogType/mongodb/catalog` | [docs](https://galaxy.starburst.io/public-api) |
| [List MySQL catalogs](actions/list-my-sql-catalogs.md) | `GET /public/api/v1/catalogType/mysql/catalog` | [docs](https://galaxy.starburst.io/public-api) |
| [List OpenSearch catalogs](actions/list-open-search-catalogs.md) | `GET /public/api/v1/catalogType/opensearch/catalog` | [docs](https://galaxy.starburst.io/public-api) |
| [List PostgreSQL catalogs](actions/list-postgresql-catalogs.md) | `GET /public/api/v1/catalogType/postgresql/catalog` | [docs](https://galaxy.starburst.io/public-api) |
| [List Redshift catalogs](actions/list-redshift-catalogs.md) | `GET /public/api/v1/catalogType/redshift/catalog` | [docs](https://galaxy.starburst.io/public-api) |
| [List role grants](actions/list-role-grants.md) | `GET /public/api/v1/role/{roleId}/rolegrant` | [docs](https://galaxy.starburst.io/public-api) |
| [List role privileges](actions/list-role-privileges.md) | `GET /public/api/v1/role/{roleId}/privilege` | [docs](https://galaxy.starburst.io/public-api) |
| [List roles](actions/list-roles.md) | `GET /public/api/v1/role` | [docs](https://galaxy.starburst.io/public-api) |
| [List S3 catalogs](actions/list-s3-catalogs.md) | `GET /public/api/v1/catalogType/s3/catalog` | [docs](https://galaxy.starburst.io/public-api) |
| [List service accounts](actions/list-service-accounts.md) | `GET /public/api/v1/serviceAccount` | [docs](https://galaxy.starburst.io/public-api) |
| [List Snowflake catalogs](actions/list-snowflake-catalogs.md) | `GET /public/api/v1/catalogType/snowflake/catalog` | [docs](https://galaxy.starburst.io/public-api) |
| [List SQL Server catalogs](actions/list-sql-server-catalogs.md) | `GET /public/api/v1/catalogType/sqlserver/catalog` | [docs](https://galaxy.starburst.io/public-api) |
| [List tags](actions/list-tags.md) | `GET /public/api/v1/tag` | [docs](https://galaxy.starburst.io/public-api) |
| [List users](actions/list-users.md) | `GET /public/api/v1/user` | [docs](https://galaxy.starburst.io/public-api) |
