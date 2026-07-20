# NetSuite - Advanced: List Locations



```
GET https://connect.mindcloud.co/v1/universal/netsuite/latest/actions/list-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetSuite - Advanced `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netsuite/latest/actions/list-locations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netsuite/latest/actions/list-locations?${params}`, {
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
| `columns` | object | no |  |
| `includeAllSublists` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NetSuite - Advanced API returns.

## Native endpoint

Through the native NetSuite - Advanced API, this operation is `POST https://{{credentials.accountId}}.restlets.api.netsuite.com/app/site/hosting/restlet.nl` (base URL `https://{{credentials.accountId}}.suitetalk.api.netsuite.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-locations.md) for the provider-specific parameters and requirements.

