# Create Offline User Data Job with Google Ads

Creates an offline user data job in Google Ads.

## Endpoint

- **Method:** `POST`
- **Path:** `v22/customers/:customerId/offlineUserDataJobs:create`
- **Base URL:** `https://googleads.googleapis.com/`
- **API:** REST
- **Official documentation:** [Create Offline User Data Job](https://developers.google.com/google-ads/api/reference/rpc/v22/OfflineUserDataJobService/CreateOfflineUserDataJob)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `list` | yes | Customer ID that owns the Google Ads resources (without dashes). |
| `job` | body | `object` | yes | Offline user data job payload (including type and metadata). |
| `validateOnly` | body | `boolean` | no | When true, validates the request without executing mutations. |
