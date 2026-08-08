# Prepare Live Call with XOi

## Endpoint

- **Method:** `POST`
- **Path:** `https://gql-live-external.xoi.io/graphql`
- **Base URL:** `https://gql-jobs-external.xoi.io/graphql`
- **Official documentation:** [Prepare Live Call](https://integration-docs.xoi.io/guides/live/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.phoneNumber` | body | `string` | yes | XOi phone number input. |
| `variables.namespace` | body | `string` | yes | XOi namespace input. |
| `variables.externalId` | body | `string` | yes | XOi external id input. |
| `variables.metadata` | body | `string` | no | XOi metadata json input. |
