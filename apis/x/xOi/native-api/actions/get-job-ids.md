# Get Job IDs with XOi

## Endpoint

- **Method:** `POST`
- **Path:** `https://gql-jobs-external.xoi.io/graphql`
- **Base URL:** `https://gql-jobs-external.xoi.io/graphql`
- **Official documentation:** [Get Job IDs](https://integration-docs.xoi.io/guides/jobs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.namespace` | body | `string` | yes | XOi namespace input. |
| `variables.externalId` | body | `string` | yes | XOi external id input. |
