# Create a termination for a lien with Middesk

Creates a lien termination in Middesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/liens/:lien_id/termination`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [Create a termination for a lien](https://docs.middesk.com/reference/businesses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lien_id` | path | `string` | yes | ID of the lien to terminate. |
