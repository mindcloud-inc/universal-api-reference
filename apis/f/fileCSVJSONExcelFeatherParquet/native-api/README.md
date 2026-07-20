# File (CSV, JSON, Excel, Feather, Parquet): Native API Reference

A consolidated summary of File (CSV, JSON, Excel, Feather, Parquet)'s API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://docs.airbyte.com/integrations/sources/file
- **API base URL:** `https://connectors.airbyte.com/files/registries/v0`

## Authentication

### None

No provider-native credentials are required for public or local file-format access. Protected storage credentials are supplied by the runtime storage location when needed.

This API does not require request authentication.

[Official authentication documentation](https://docs.airbyte.com/integrations/sources/file)

## API conventions

Responses from this API use JSON.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Build Azure Blob File Config](actions/build-azure-blob-file-config.md) | `GET /oss_registry.json` | [docs](https://docs.airbyte.com/integrations/sources/file#azblob-azure-blob-storage) |
| [Build GCS File Config](actions/build-gcs-file-config.md) | `GET /oss_registry.json` | [docs](https://docs.airbyte.com/integrations/sources/file#gcs-google-cloud-storage) |
| [Build HTTPS File Config](actions/build-https-file-config.md) | `GET /oss_registry.json` | [docs](https://docs.airbyte.com/integrations/sources/file#https-public-web-default) |
| [Build Local File Config](actions/build-local-file-config.md) | `GET /oss_registry.json` | [docs](https://docs.airbyte.com/integrations/sources/file#local-filesystem-airbyte-open-source-only) |
| [Build S3 File Config](actions/build-s3-file-config.md) | `GET /oss_registry.json` | [docs](https://docs.airbyte.com/integrations/sources/file#s3-amazon-web-services) |
| [Build SCP File Config](actions/build-scp-file-config.md) | `GET /oss_registry.json` | [docs](https://docs.airbyte.com/integrations/sources/file#ssh-secure-shell--scp-secure-copy-protocol--sftp-secure-file-transfer-protocol) |
| [Build SFTP File Config](actions/build-sftp-file-config.md) | `GET /oss_registry.json` | [docs](https://docs.airbyte.com/integrations/sources/file#ssh-secure-shell--scp-secure-copy-protocol--sftp-secure-file-transfer-protocol) |
| [Build SSH File Config](actions/build-ssh-file-config.md) | `GET /oss_registry.json` | [docs](https://docs.airbyte.com/integrations/sources/file#ssh-secure-shell--scp-secure-copy-protocol--sftp-secure-file-transfer-protocol) |
| [Check File Access / Connectivity](actions/check-file-access-connectivity.md) | `GET /oss_registry.json` | [docs](https://docs.airbyte.com/integrations/sources/file#step-3-complete-the-connector-setup) |
| [Get File Connector Metadata](actions/get-file-connector-metadata.md) | `GET /oss_registry.json` | [docs](https://docs.airbyte.com/integrations/sources/file) |
| [Get File Source Spec](actions/get-file-source-spec.md) | `GET /oss_registry.json` | [docs](https://docs.airbyte.com/integrations/sources/file#config-fields-reference) |
| [Get Supported File Formats](actions/get-supported-file-formats.md) | `GET /oss_registry.json` | [docs](https://docs.airbyte.com/integrations/sources/file#file-formats) |
| [Get Supported Storage Providers](actions/get-supported-storage-providers.md) | `GET /oss_registry.json` | [docs](https://docs.airbyte.com/integrations/sources/file#storage-providers) |
| [Infer File Schema](actions/infer-file-schema.md) | `GET /oss_registry.json` | [docs](https://docs.airbyte.com/integrations/sources/file#step-3-complete-the-connector-setup) |
| [List Available Streams](actions/list-available-streams.md) | `GET /oss_registry.json` | [docs](https://airbyte.com/pyairbyte/file-python) |
| [Preview File Rows](actions/preview-file-rows.md) | `GET /oss_registry.json` | [docs](https://airbyte.com/pyairbyte/file-python) |
| [Validate File Source Configuration](actions/validate-file-source-configuration.md) | `GET /oss_registry.json` | [docs](https://docs.airbyte.com/integrations/sources/file#prerequisites) |
