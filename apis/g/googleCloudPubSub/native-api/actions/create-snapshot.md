# Create Snapshot with Google Cloud Pub/Sub

Creates a snapshot in Google Cloud Pub/Sub.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/:name`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Create Snapshot](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.snapshots/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Required. User-provided name for this snapshot. Format is `projects/{project}/snapshots/{snap}`. |
