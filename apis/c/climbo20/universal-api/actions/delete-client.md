# Climbo 2.0: Delete Client

Deletes a client from Climbo 2.0.

```
DELETE https://connect.mindcloud.co/v1/universal/climbo20/latest/actions/delete-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Climbo 2.0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/climbo20/latest/actions/delete-client?connectionId=$CONNECTION_ID&clientId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/climbo20/latest/actions/delete-client?${params}`, {
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
| `clientId` | string | yes | ID of your customer. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Climbo 2.0 API returns.

## Native endpoint

Through the native Climbo 2.0 API, this operation is `DELETE /client/{client_id}` (base URL `https://api.climbo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-client.md) for the provider-specific parameters and requirements.

