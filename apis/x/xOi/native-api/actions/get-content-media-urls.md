# Get Content Media URLs with XOi

## Endpoint

- **Method:** `POST`
- **Path:** `https://gql-content-external.xoi.io/graphql`
- **Base URL:** `https://gql-jobs-external.xoi.io/graphql`
- **Official documentation:** [Get Content Media URLs](https://integration-docs.xoi.io/guides/enhanced_content_api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.contentIds[]` | body | `array<string>` | yes | XOi content IDs to retrieve, up to 50. Send multiple values as a array. |
