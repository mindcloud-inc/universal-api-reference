# Viewpoint Vista: Search AP Objects

Search objects found in the Viewpoint® Vista™ Accounts Payable (AP) programs.

```
GET https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/search-ap-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewpoint Vista `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/search-ap-objects?connectionId=$CONNECTION_ID&limit=25&offset=0&object=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "object": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viewpointVista/latest/actions/search-ap-objects?${params}`, {
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
| `modifiedUtcAfter` | date | no | Specify a datetime against which to filter the results. |
| `modifiedUtcBefore` | date | no | Specify a datetime against which to filter the results. |
| `object` | list<string> | yes | Specify the type of Object from the Accounts Payable V2 Direct API that you'd like to retrieve. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viewpoint Vista API returns.

## Native endpoint

Through the native Viewpoint Vista API, this operation is `POST v1/direct/subscribers/:subscriber_code/vista/:api/2/data/:object/cache/search` (base URL `https://api.xchange.trimble.com/connect/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-ap-objects.md) for the provider-specific parameters and requirements.

