# Crossmint: Get Action Status

Retrieves action status from Crossmint.

```
GET https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/get-action-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crossmint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/get-action-status?connectionId=$CONNECTION_ID&actionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "actionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crossmint/latest/actions/get-action-status?${params}`, {
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
| `actionId` | string | yes | Asynchronous action identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Crossmint API returns.

## Native endpoint

Through the native Crossmint API, this operation is `GET /2022-06-09/actions/:actionId` (base URL `https://staging.crossmint.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-action-status.md) for the provider-specific parameters and requirements.

