# Store Media Asset with RICOH360 Tours

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://bbomwcm27nhalfwjvwzy6qbrim.appsync-api.us-west-2.amazonaws.com`
- **Official documentation:** [Store Media Asset](https://www.ricoh360.com/developer/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucket` | query | `string` | no | Storage bucket for the asset. |
| `key` | query | `string` | no | Storage object key for the asset. |
| `region` | query | `string` | no | Storage region for the asset. |
| `url` | query | `string` | no | Source file URL to store. |
