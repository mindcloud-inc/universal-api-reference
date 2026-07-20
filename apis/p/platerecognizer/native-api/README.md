# Platerecognizer: Native API Reference

A consolidated summary of Platerecognizer's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://guides.platerecognizer.com/
- **API base URL:** `https://api.platerecognizer.com/v1`

## Authentication

### API Key

Use your Plate Recognizer Snapshot Cloud API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://guides.platerecognizer.com/docs/snapshot/api-reference/)

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Blur Plates And Faces In Image](actions/blur-plates-and-faces-in-image.md) | `POST https://blur.platerecognizer.com/v1/blur` | [docs](https://guides.platerecognizer.com/docs/other-apps/blur/api-reference/#blur-plates-and-faces-in-an-image) |
| [Create Camera Monitoring Log](actions/create-camera-monitoring-log.md) | `POST /vision-alert/create-log/` | [docs](https://guides.platerecognizer.com/docs/other-apps/vision-alert/api-reference/#create-camera-monitoring-log) |
| [Extract Text From Image](actions/extract-text-from-image.md) | `POST /ocr/reader/` | [docs](https://guides.platerecognizer.com/docs/other-apps/ocr/api-reference/#extract-text-from-an-image) |
| [Get OCR Statistics](actions/get-ocr-statistics.md) | `GET /ocr/statistics/` | [docs](https://guides.platerecognizer.com/docs/other-apps/ocr/api-reference/#statistics) |
| [Get Statistics](actions/get-statistics.md) | `GET /statistics/` | [docs](https://guides.platerecognizer.com/docs/snapshot/api-reference/#statistics) |
| [Get VIN Statistics](actions/get-vin-statistics.md) | `GET /vin/statistics/` | [docs](https://guides.platerecognizer.com/docs/other-apps/vin-id/api-reference/#statistics) |
| [Read Number Plates From Image](actions/read-number-plates-from-image.md) | `POST /plate-reader/` | [docs](https://guides.platerecognizer.com/docs/snapshot/api-reference/#read-number-plates-from-an-image) |
| [Read VIN From Image](actions/read-vin-from-image.md) | `POST /vin/reader/` | [docs](https://guides.platerecognizer.com/docs/other-apps/vin-id/api-reference/#read-vin-from-an-image) |
| [Upload Video For Stream Cloud](actions/upload-video-for-stream-cloud.md) | `POST /stream/video-upload/` | [docs](https://guides.platerecognizer.com/docs/stream/cloud/video-upload-api/#http-request) |
