# 3E Protect: Get Location by ID



```
GET https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/get-location-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 3E Protect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/get-location-by-id?connectionId=$CONNECTION_ID&locationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eProtect/latest/actions/get-location-by-id?${params}`, {
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
| `locationId` | string | yes | Location ID returned by List Locations. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 3E Protect API returns.

## Native endpoint

Through the native 3E Protect API, this operation is `GET /location/id/:locationId` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-location-by-id.md) for the provider-specific parameters and requirements.

