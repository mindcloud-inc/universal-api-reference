# List Buckets with Google Cloud Storage

Retrieves a list of buckets from Google Cloud Storage.

## Endpoint

- **Method:** `GET`
- **Path:** `/storage/v1/b`
- **Base URL:** `https://storage.googleapis.com`
- **Official documentation:** [List Buckets](https://docs.cloud.google.com/storage/docs/json_api/v1/buckets/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prefix` | query | `string` | no | Optional bucket name prefix to restrict results. |
