# EMnify: List SIMs

Retrieves a list of SIMs from EMnify.

```
GET https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/list-sims
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EMnify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/list-sims?connectionId=$CONNECTION_ID&limit=25&offset=0&authToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "authToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/list-sims?${params}`, {
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
| `authToken` | string | yes | Auth token from Retrieve Authentication Token. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `searchQuery` | string | no | Filter SIMs by search query. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EMnify API returns.

## Native endpoint

Through the native EMnify API, this operation is `GET /sim` (base URL `https://cdn.emnify.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sims.md) for the provider-specific parameters and requirements.

