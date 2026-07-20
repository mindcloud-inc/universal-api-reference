# Create Destination Connection Check with Unstructured

Creates a destination connection check in Unstructured.

## Endpoint

- **Method:** `POST`
- **Path:** `/destinations/:destination_id/connection-check`
- **Base URL:** `https://platform.unstructuredapp.io/api/v1`
- **Official documentation:** [Create Destination Connection Check](https://docs.unstructured.io/api-reference/destinations/create-destination-connection-check)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destination_id` | path | `string` | yes | The destination connector ID. |
