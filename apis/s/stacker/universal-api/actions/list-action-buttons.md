# Stacker: List Action Buttons

Retrieves action buttons for a Stacker object.

```
GET https://connect.mindcloud.co/v1/universal/stacker/latest/actions/list-action-buttons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stacker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stacker/latest/actions/list-action-buttons?connectionId=$CONNECTION_ID&accountId=string&objectSid=string&stackId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string",
  "objectSid": "string",
  "stackId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stacker/latest/actions/list-action-buttons?${params}`, {
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
| `accountId` | string | yes | Stacker account ID sent as the X-Account-Id header. |
| `objectSid` | string | yes | Object SID from the Stacker endpoint path. |
| `stackId` | string | yes | Stacker stack ID sent as the X-Stack-Id header. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Stacker API returns.

## Native endpoint

Through the native Stacker API, this operation is `GET /api/external/objects/:object_sid/action-buttons/` (base URL `https://api.go.stackerhq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-action-buttons.md) for the provider-specific parameters and requirements.

