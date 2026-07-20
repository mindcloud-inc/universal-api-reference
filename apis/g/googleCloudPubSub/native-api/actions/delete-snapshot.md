# Delete Snapshot with Google Cloud Pub/Sub

Deletes a snapshot from Google Cloud Pub/Sub.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/:snapshot`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Delete Snapshot](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.snapshots/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `snapshot` | path | `string` | yes | Required. The name of the snapshot to delete. Format is `projects/{project}/snapshots/{snap}`. |
