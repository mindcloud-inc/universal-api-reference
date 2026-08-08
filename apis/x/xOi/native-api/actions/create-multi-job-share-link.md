# Create Multi-Job Share Link with XOi

## Endpoint

- **Method:** `POST`
- **Path:** `https://gql-share-external.xoi.io/graphql`
- **Base URL:** `https://gql-jobs-external.xoi.io/graphql`
- **Official documentation:** [Create Multi-Job Share Link](https://integration-docs.xoi.io/guides/share/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.jobIds[]` | body | `array<string>` | yes | XOi job ids input. |
