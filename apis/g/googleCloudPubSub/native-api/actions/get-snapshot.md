# Get Snapshot with Google Cloud Pub/Sub

Retrieves a snapshot from Google Cloud Pub/Sub.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/:snapshot`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Get Snapshot](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.snapshots/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `snapshot` | path | `string` | yes | Required. The name of the snapshot to get. Format is `projects/{project}/snapshots/{snap}`. |
