# GraphQL endpoint with Appwrite

Makes a GraphQL query request to Appwrite.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [GraphQL endpoint](https://appwrite.io/docs/references/cloud/server-rest/graphql)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | GraphQL query string. |
