# Loggly (Send Data): Native API Reference

A consolidated summary of Loggly (Send Data)'s API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://documentation.solarwinds.com/en/success_center/loggly/content/admin/api-sending-data.htm
- **API base URL:** `https://logs-01.loggly.com`

## Authentication

### Customer Token

Use a Loggly customer token for HTTP/S ingestion requests.

[Official authentication documentation](https://documentation.solarwinds.com/en/success_center/loggly/content/admin/customer-token-authentication-token.htm)

## API conventions

Responses from this API use JSON.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Send Bulk Events](actions/send-bulk-events.md) | `POST /bulk/:customerToken/tag/:tagPath/` | [docs](https://documentation.solarwinds.com/en/success_center/loggly/content/admin/api-sending-data.htm) |
| [Send JSON Event](actions/send-json-event.md) | `POST /inputs/:customerToken/tag/:tagPath/` | [docs](https://documentation.solarwinds.com/en/success_center/loggly/content/admin/api-sending-data.htm) |
| [Send Multiline Event](actions/send-multiline-event.md) | `POST /inputs/:customerToken/tag/:tagPath/` | [docs](https://documentation.solarwinds.com/en/success_center/loggly/content/admin/http-endpoint.htm) |
| [Send Plaintext Event](actions/send-plaintext-event.md) | `POST /inputs/:customerToken/tag/:tagPath/` | [docs](https://documentation.solarwinds.com/en/success_center/loggly/content/admin/api-sending-data.htm) |
| [Send Tracking Pixel Event](actions/send-tracking-pixel-event.md) | `GET /inputs/:customerToken.gif` | [docs](https://documentation.solarwinds.com/en/success_center/loggly/content/admin/tracking-pixel.htm) |
| [Upload Log File](actions/upload-log-file.md) | `POST /bulk/:customerToken/tag/:tagPath/` | [docs](https://documentation.solarwinds.com/en/success_center/loggly/content/admin/file-upload.htm) |
