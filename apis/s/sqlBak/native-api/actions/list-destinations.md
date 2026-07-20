# List Destinations with SqlBak

Retrieves destinations from SqlBak.

## Endpoint

- **Method:** `GET`
- **Path:** `/destinations`
- **Base URL:** `https://sqlbak.com/public-api/v1`
- **Official documentation:** [List Destinations](https://sqlbak.docs.apiary.io/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `server_id` | query | `number` | no | Filter destinations by server ID. |
| `job_id` | query | `number` | no | Filter destinations by job ID. |
| `destination_type` | query | `list` | no | Filter destinations by destination type. Accepted values: `amazon_s3`, `azure_storage`, `backblaze_b2`, `box`, `dropbox`, `folder`, `ftp`, `google_drive`, `onedrive`, `onedrive_for_business`, `s3_compatible`, `yandex_disk`. |
