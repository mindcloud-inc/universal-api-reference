# GSA Site Scanning: Native API Reference

A consolidated summary of GSA Site Scanning's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://www.developer.aero/api-catalog/flex/scan-api-v2
- **OpenAPI specification:** https://www.developer.aero/system/files/2022-11/SITA-Flex-ScanAPI_V2.json
- **API base URL:** `https://api.sitaflex.aero`

## Authentication

### No Authentication

The public SITA Flex Scan OpenAPI specification declares no security scheme. Access to Flex itself must be requested and approved through developer.aero before runtime use.

This API does not require request authentication.

[Official authentication documentation](https://www.developer.aero/docs/requesting-api-access)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Scan Device](actions/get-scan-device.md) | `GET /scan/v2/device/:deviceId` | [docs](https://www.developer.aero/api-catalog/flex/scan-api-v2) |
| [Start Scanning](actions/start-scanning.md) | `POST /scan/v2/startscanning` | [docs](https://www.developer.aero/api-catalog/flex/scan-api-v2) |
| [Stop Scanning](actions/stop-scanning.md) | `POST /scan/v2/stopscanning` | [docs](https://www.developer.aero/api-catalog/flex/scan-api-v2) |
