# Google BigQuery: Native API Reference

A consolidated summary of Google BigQuery's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://bigquery.googleapis.com/$discovery/rest?version=v2

## Authentication

### Google BigQuery connection

### Credentials

- **Project:** `projectId` · required · Project ID
- **Client Email:** `clientEmail` · required
- **Private Key:** `privateKey` · required
- **Location:** `location` · optional · US by default. If your dataset is not from the US region (e.g., it’s EU or us-central1) you can get it by going to the BigQuery Console → your dataset → Details → Location.

Pass these values to the database driver when opening the connection. This is a driver connection rather than HTTP authentication, so there is no `Authorization` header.

## Endpoints (1 documented)

| Operation | Method & path |
| --- | --- |
| [Query](actions/query.md) | `GET` |
