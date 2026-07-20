# NetSuite - Advanced: Search using Saved Search

Search using a previously saved search using NetSuite's Query Language

```
GET https://connect.mindcloud.co/v1/universal/netsuite/latest/actions/get-saved-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetSuite - Advanced `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netsuite/latest/actions/get-saved-search?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netsuite/latest/actions/get-saved-search?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `savedSearchId` | list | no |  |
| `savedSearchLink` | object | no | This is a display only component. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `savedSearchType` | string | no | Some saved searches (like Inventory Balance or System Notes) aren’t tied to a record type, so NetSuite can’t determine their type automatically. Providing the saved search type ensures the search can be loaded and executed correctly. |
| `includeIds` | boolean | no | Return the ID value of lookups in addition to their text labels. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NetSuite - Advanced API returns.

## Native endpoint

Through the native NetSuite - Advanced API, this operation is `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` (base URL `https://{{credentials.accountId}}.suitetalk.api.netsuite.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-saved-search.md) for the provider-specific parameters and requirements.

