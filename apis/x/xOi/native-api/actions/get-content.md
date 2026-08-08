# Get Content with XOi

## Endpoint

- **Method:** `POST`
- **Path:** `https://gql-content-external.xoi.io/graphql`
- **Base URL:** `https://gql-jobs-external.xoi.io/graphql`
- **Official documentation:** [Get Content](https://integration-docs.xoi.io/guides/content/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.contentIds[]` | body | `array<string>` | yes | XOi content ids input. |
