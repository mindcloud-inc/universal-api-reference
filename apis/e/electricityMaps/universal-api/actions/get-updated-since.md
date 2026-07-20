# Electricity Maps: Get Updated Since



```
GET https://connect.mindcloud.co/v1/universal/electricityMaps/latest/actions/get-updated-since
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Electricity Maps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/electricityMaps/latest/actions/get-updated-since?connectionId=$CONNECTION_ID&zone=string&since=string&start=string&end=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "zone": "string",
  "since": "string",
  "start": "string",
  "end": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/electricityMaps/latest/actions/get-updated-since?${params}`, {
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
| `zone` | string | yes |  |
| `since` | string | yes |  |
| `start` | string | yes |  |
| `end` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Electricity Maps API returns.

## Native endpoint

Through the native Electricity Maps API, this operation is `GET /updated-since` (base URL `https://api.electricitymaps.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-updated-since.md) for the provider-specific parameters and requirements.

