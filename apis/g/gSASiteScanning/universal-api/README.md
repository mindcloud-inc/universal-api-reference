# GSA Site Scanning: Universal API

Use SITA Flex Scan API to read travel documents, barcodes, and frequent flyer cards from supported scan devices.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gSASiteScanning/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.developer.aero/api-catalog/flex/scan-api/overview
- **Vendor API docs:** https://www.developer.aero/api-catalog/flex/scan-api-v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Scan Device](actions/get-scan-device.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gSASiteScanning/latest/actions/get-scan-device?connectionId=$CONNECTION_ID&deviceId=scanner-123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Device

| Action | Method | Description |
| --- | --- | --- |
| [Get Scan Device](actions/get-scan-device.md) | GET | Retrieves a scan device by device ID. |
| [Start Scanning](actions/start-scanning.md) | PUT | Requests a scan device to start sending scan data. |
| [Stop Scanning](actions/stop-scanning.md) | PUT | Requests a scan device to stop sending scan data. |

