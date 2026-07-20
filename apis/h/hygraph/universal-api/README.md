# <img src="https://images.mindcloud.co/apps/icons/hygraph_1776179987840.png" alt="Hygraph logo" width="28" height="28"> Hygraph: Universal API

Hygraph is a headless CMS for creating, managing, and delivering structured content through GraphQL APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hygraph/latest
- **Category:** Marketing
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://hygraph.com
- **Vendor API docs:** https://hygraph.com/docs/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Introspect Schema](actions/introspect-schema.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hygraph/latest/actions/introspect-schema?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Create Asset From Remote URL](actions/create-asset-from-remote-url.md) | POST | Creates a new asset from a remote URL in Hygraph. |
| [Delete Asset](actions/delete-asset.md) | DELETE | Deletes an existing asset from Hygraph. |
| [Get Asset](actions/get-asset.md) | GET | Retrieves an asset from Hygraph. |
| [List Assets](actions/list-assets.md) | GET | Retrieves assets from Hygraph. |
| [Publish Asset](actions/publish-asset.md) | PUT | Publishes an asset to content stages in Hygraph. |
| [Unpublish Asset](actions/unpublish-asset.md) | PUT | Unpublishes an asset from content stages in Hygraph. |
| [Update Asset Remote URL](actions/update-asset-remote-url.md) | PUT | Updates an existing asset from a remote URL in Hygraph. |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [Execute GraphQL Mutation](actions/execute-graphql-mutation.md) | POST | Executes a GraphQL mutation in Hygraph. |
| [Execute GraphQL Query](actions/execute-graphql-query.md) | GET | Executes a GraphQL query in Hygraph. |
| [Introspect Schema](actions/introspect-schema.md) | GET | Retrieves GraphQL schema details from Hygraph. |

