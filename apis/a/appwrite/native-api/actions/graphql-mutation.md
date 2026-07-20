# GraphQL endpoint with Appwrite

Makes a GraphQL mutation request to Appwrite.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql/mutation`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [GraphQL endpoint](https://appwrite.io/docs/references/cloud/server-rest/graphql)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | GraphQL mutation string. |
