# <img src="https://images.mindcloud.co/apps/icons/sourcegraph_1776799430191.png" alt="Sourcegraph logo" width="28" height="28"> Sourcegraph: Universal API

Search, navigate, and analyze code across repositories

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sourcegraph/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sourcegraph.com
- **Vendor API docs:** https://sourcegraph.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sourcegraph/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization By Name](actions/get-organization-by-name.md) | GET | Retrieves an organization from Sourcegraph by name. |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [Create Saved Search](actions/create-saved-search.md) | POST | Creates a saved search in Sourcegraph. |
| [Create Search Context](actions/create-search-context.md) | POST | Creates a search context in Sourcegraph. |
| [Delete Saved Search](actions/delete-saved-search.md) | DELETE | Deletes a saved search from Sourcegraph. |
| [Delete Search Context](actions/delete-search-context.md) | DELETE | Deletes a search context from Sourcegraph. |
| [Get Search Context By Spec](actions/get-search-context-by-spec.md) | GET | Retrieves a search context from Sourcegraph by spec. |
| [List Saved Searches](actions/list-saved-searches.md) | GET | Retrieves saved searches from Sourcegraph. |
| [List Search Contexts](actions/list-search-contexts.md) | GET | Retrieves search contexts from Sourcegraph. |
| [Parse Search Query](actions/parse-search-query.md) | GET | Parses a search query in Sourcegraph. |
| [Run Search](actions/run-search.md) | GET | Runs a search in Sourcegraph. |
| [Update Saved Search](actions/update-saved-search.md) | PUT | Updates a saved search in Sourcegraph. |
| [Update Search Context](actions/update-search-context.md) | PUT | Updates a search context in Sourcegraph. |

### Repositories

| Action | Method | Description |
| --- | --- | --- |
| [Get Repository By Name](actions/get-repository-by-name.md) | GET | Retrieves a repository from Sourcegraph by name. |
| [List Repositories](actions/list-repositories.md) | GET | Retrieves repositories from Sourcegraph. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Client Configuration](actions/get-client-configuration.md) | GET | Retrieves client configuration from Sourcegraph. |
| [Get Namespace By Name](actions/get-namespace-by-name.md) | GET | Retrieves a namespace from Sourcegraph by name. |
| [Get Site Info](actions/get-site-info.md) | GET | Retrieves site information from Sourcegraph. |
| [Get Viewer Settings](actions/get-viewer-settings.md) | GET | Retrieves viewer settings from Sourcegraph. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Sourcegraph. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User By Username](actions/get-user-by-username.md) | GET | Retrieves a user from Sourcegraph by username. |

