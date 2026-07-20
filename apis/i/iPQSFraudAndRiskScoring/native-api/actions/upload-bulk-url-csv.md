# Upload Bulk URL CSV with IPQS Fraud and Risk Scoring

Uploads a bulk URL scan CSV to IPQS.

## Endpoint

- **Method:** `POST`
- **Path:** `/csv/upload`
- **Base URL:** `https://www.ipqualityscore.com/api/json`
- **Official documentation:** [Upload Bulk URL CSV](https://www.ipqualityscore.com/documentation/csv-api/uploading-csvs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_name` | body | `string` | no | Optional name for the uploaded CSV. |
| `input[]` | body | `array<array>` | yes | Rows to upload for processing as JSON. |
