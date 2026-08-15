# Samsara: List Driver-Vehicle Assignments



```
GET https://connect.mindcloud.co/v1/universal/samsara/latest/actions/list-driver-vehicle-assignments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Samsara `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/samsara/latest/actions/list-driver-vehicle-assignments?connectionId=$CONNECTION_ID&limit=25&offset=0&filterBy=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "filterBy": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/samsara/latest/actions/list-driver-vehicle-assignments?${params}`, {
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
| `filterBy` | string | yes | Whether to filter assignments by drivers or vehicles. |
| `startTime` | string | no | Assignment range start in RFC 3339 format. |
| `endTime` | string | no | Assignment range end in RFC 3339 format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Samsara API returns.

## Native endpoint

Through the native Samsara API, this operation is `GET fleet/driver-vehicle-assignments` (base URL `https://api.samsara.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-driver-vehicle-assignments.md) for the provider-specific parameters and requirements.

