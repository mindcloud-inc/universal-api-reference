# Get Schema with Google Cloud Pub/Sub

Retrieves a schema from Google Cloud Pub/Sub.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/:name`
- **Base URL:** `https://pubsub.googleapis.com`
- **Official documentation:** [Get Schema](https://docs.cloud.google.com/pubsub/docs/reference/rest/v1/projects.schemas/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | Required. The name of the schema to get. Format is `projects/{project}/schemas/{schema}`. |
| `view` | query | `string` | no | The set of fields to return in the response. If not set, returns a Schema with all fields filled out. Set to `BASIC` to omit the `definition`. |
