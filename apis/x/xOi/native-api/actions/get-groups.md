# Get Groups with XOi

## Endpoint

- **Method:** `POST`
- **Path:** `https://gql-users-external.xoi.io/graphql`
- **Base URL:** `https://gql-jobs-external.xoi.io/graphql`
- **Official documentation:** [Get Groups](https://integration-docs.xoi.io/guides/users/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.ids[]` | body | `array<string>` | yes | XOi group ids input. |
