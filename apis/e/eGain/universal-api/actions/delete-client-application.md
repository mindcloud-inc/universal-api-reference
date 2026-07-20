# eGain: Delete Client Application

Deletes an existing client application from eGain.

```
DELETE https://connect.mindcloud.co/v1/universal/eGain/latest/actions/delete-client-application
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/eGain/latest/actions/delete-client-application?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eGain/latest/actions/delete-client-application?${params}`, {
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
| `id` | string | yes | Client application ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native eGain API returns.

## Native endpoint

Through the native eGain API, this operation is `DELETE /clientapplications/:id` (base URL `https://api.ai.egain.cloud/conversation/conversationmgr/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-client-application.md) for the provider-specific parameters and requirements.

