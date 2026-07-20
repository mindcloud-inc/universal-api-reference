# EMnify: List Endpoint Events

Retrieves events for an endpoint from EMnify.

```
GET https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/list-endpoint-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EMnify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/list-endpoint-events?connectionId=$CONNECTION_ID&limit=25&offset=0&authToken=string&endpointId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "authToken": "string",
  "endpointId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/list-endpoint-events?${params}`, {
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
| `endpointId` | number | yes | Numeric ID of an endpoint. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `q` | string | no | Optional event filter in <filter>:<value> format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EMnify API returns.

## Native endpoint

Through the native EMnify API, this operation is `GET /endpoint/:endpoint_id/event` (base URL `https://cdn.emnify.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-endpoint-events.md) for the provider-specific parameters and requirements.

