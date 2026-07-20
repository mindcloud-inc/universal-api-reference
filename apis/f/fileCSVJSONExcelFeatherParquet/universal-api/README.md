# <img src="https://images.mindcloud.co/apps/icons/icon-2_1777323457445.png" alt="File (CSV, JSON, Excel, Feather, Parquet) logo" width="28" height="28"> File (CSV, JSON, Excel, Feather, Parquet): Universal API

Parse and inspect CSV, JSON, Excel, Feather, and Parquet files

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fileCSVJSONExcelFeatherParquet/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://airbyte.com
- **Vendor API docs:** https://docs.airbyte.com/integrations/sources/file

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get File Connector Metadata](actions/get-file-connector-metadata.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fileCSVJSONExcelFeatherParquet/latest/actions/get-file-connector-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### File Connector Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get File Connector Metadata](actions/get-file-connector-metadata.md) | GET | Retrieves metadata for the File source connector. |

### File Row Preview

| Action | Method | Description |
| --- | --- | --- |
| [Preview File Rows](actions/preview-file-rows.md) | GET | Retrieves preview rows from a file source. |

### File Schema

| Action | Method | Description |
| --- | --- | --- |
| [Infer File Schema](actions/infer-file-schema.md) | GET | Retrieves an inferred schema for a file source. |

### File Source Config

| Action | Method | Description |
| --- | --- | --- |
| [Build Azure Blob File Config](actions/build-azure-blob-file-config.md) | POST | Creates an Azure Blob file source configuration. |
| [Build GCS File Config](actions/build-gcs-file-config.md) | POST | Creates a GCS file source configuration. |
| [Build HTTPS File Config](actions/build-https-file-config.md) | POST | Creates an HTTPS file source configuration. |
| [Build Local File Config](actions/build-local-file-config.md) | POST | Creates a local file source configuration. |
| [Build S3 File Config](actions/build-s3-file-config.md) | POST | Creates an S3 file source configuration. |
| [Build SCP File Config](actions/build-scp-file-config.md) | POST | Creates an SCP file source configuration. |
| [Build SFTP File Config](actions/build-sftp-file-config.md) | POST | Creates an SFTP file source configuration. |
| [Build SSH File Config](actions/build-ssh-file-config.md) | POST | Creates an SSH file source configuration. |
| [Check File Access / Connectivity](actions/check-file-access-connectivity.md) | GET | Retrieves connectivity guidance for a file source. |
| [Validate File Source Configuration](actions/validate-file-source-configuration.md) | GET | Retrieves validation requirements for a file source configuration. |

### File Source Spec

| Action | Method | Description |
| --- | --- | --- |
| [Get File Source Spec](actions/get-file-source-spec.md) | GET | Retrieves the File source specification. |

### File Stream

| Action | Method | Description |
| --- | --- | --- |
| [List Available Streams](actions/list-available-streams.md) | GET | Retrieves available streams for a file source. |

### Supported File Format

| Action | Method | Description |
| --- | --- | --- |
| [Get Supported File Formats](actions/get-supported-file-formats.md) | GET | Retrieves supported file formats for the File source. |

### Supported Storage Provider

| Action | Method | Description |
| --- | --- | --- |
| [Get Supported Storage Providers](actions/get-supported-storage-providers.md) | GET | Retrieves supported storage providers for the File source. |

