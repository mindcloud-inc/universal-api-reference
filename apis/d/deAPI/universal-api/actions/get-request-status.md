# deAPI: Get Request Status

Retrieves the status of an inference job from deAPI.

```
GET https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/get-request-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a deAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/get-request-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deAPI/latest/actions/get-request-status?${params}`, {
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
| `requestId` | string | no | The deAPI request identifier to inspect. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native deAPI API returns.

## Native endpoint

Through the native deAPI API, this operation is `GET /api/v1/client/request-status/:request_id` (base URL `https://api.deapi.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-request-status.md) for the provider-specific parameters and requirements.

