# <img src="https://images.mindcloud.co/apps/icons/fibery_1774038030948.png" alt="Fibery logo" width="28" height="28"> Fibery: Universal API

Query, manage, and automate Fibery workspaces and records

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fibery/latest
- **Category:** Productivity / Project Management
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://fibery.io
- **Vendor API docs:** https://the.fibery.io/@public/User_Guide/Guide/Fibery-API-Overview-279

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Schema](actions/get-schema.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fibery/latest/actions/get-schema?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Entity

| Action | Method | Description |
| --- | --- | --- |
| [Create Entity](actions/create-entity.md) | POST | Creates a new entity in Fibery. |
| [Create Or Update Entities](actions/create-or-update-entities.md) | PUT | Creates or updates entities in Fibery. |
| [Delete Entity](actions/delete-entity.md) | DELETE | Deletes an existing entity from Fibery. |
| [Query Entities](actions/query-entities.md) | GET | Retrieves entities from Fibery. |
| [Update Entity](actions/update-entity.md) | PUT | Updates an existing entity in Fibery. |

### Entity Collection

| Action | Method | Description |
| --- | --- | --- |
| [Add Collection Items](actions/add-collection-items.md) | PUT | Adds collection items to an entity in Fibery. |
| [Remove Collection Items](actions/remove-collection-items.md) | PUT | Removes collection items from an entity in Fibery. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Field](actions/create-field.md) | POST | Creates a new field in Fibery. |
| [Delete Field](actions/delete-field.md) | DELETE | Deletes an existing field from Fibery. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Attach File To Entity](actions/attach-file-to-entity.md) | PUT | Attaches a file to an entity in Fibery. |
| [Download File](actions/download-file.md) | GET | Retrieves a file from Fibery. |
| [Get Temporary Public File URLs](actions/get-temporary-public-file-urls.md) | GET | Retrieves temporary public file URLs from Fibery. |
| [Upload File](actions/upload-file.md) | POST | Creates a new file in Fibery. |
| [Upload File From URL](actions/upload-file-from-url.md) | POST | Creates a new file in Fibery from a URL. |

### Graphql

| Action | Method | Description |
| --- | --- | --- |
| [GraphQL Mutation](actions/graphql-mutation.md) | PUT | Updates data in Fibery using GraphQL. |
| [GraphQL Query](actions/graphql-query.md) | GET | Retrieves query results from Fibery GraphQL. |

### Graphql Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [List GraphQL Endpoints](actions/list-graphql-endpoints.md) | GET | Retrieves GraphQL endpoint details from Fibery. |

### Schema

| Action | Method | Description |
| --- | --- | --- |
| [Get Schema](actions/get-schema.md) | GET | Retrieves a schema from Fibery. |

### Type

| Action | Method | Description |
| --- | --- | --- |
| [Create Type](actions/create-type.md) | POST | Creates a new type in Fibery. |
| [Delete Type](actions/delete-type.md) | DELETE | Deletes an existing type from Fibery. |
| [Rename Type](actions/rename-type.md) | PUT | Updates an existing type in Fibery. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Fibery. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Fibery. |

