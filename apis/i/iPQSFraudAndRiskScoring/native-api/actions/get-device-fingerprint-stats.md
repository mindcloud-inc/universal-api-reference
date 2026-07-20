# Get Device Fingerprint Stats with IPQS Fraud and Risk Scoring

Retrieves device fingerprint statistics from IPQS.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/ExampleIntegration/json/device_tracker_statistics`
- **Base URL:** `https://www.ipqualityscore.com/api/json`
- **Official documentation:** [Get Device Fingerprint Stats](https://www.ipqualityscore.com/documentation/integrations/device-tracker-statistics)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | body | `string` | yes | Site domain or domain that requested the custom integration. |
| `secret` | body | `string` | yes | User secret created during the IPQS custom integration authentication process. |
| `domain` | body | `string` | no | Optional domain to fetch trackers for. |
| `start` | body | `date` | no | Optional start date in YYYY-MM-DD format. |
| `stop` | body | `date` | no | Optional stop date in YYYY-MM-DD format, no more than 90 days from start. |
| `tracker_name` | body | `string` | no | Optional exact tracker name to fetch. |
