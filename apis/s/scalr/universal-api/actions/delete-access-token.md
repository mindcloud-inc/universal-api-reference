# Scalr: Delete Access Token

Deletes an access token from Scalr.

```
DELETE https://connect.mindcloud.co/v1/universal/scalr/latest/actions/delete-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scalr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/scalr/latest/actions/delete-access-token?connectionId=$CONNECTION_ID&access_token=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "access_token": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scalr/latest/actions/delete-access-token?${params}`, {
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
| `access_token` | string | yes | Scalr access token ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Scalr API returns.

## Native endpoint

Through the native Scalr API, this operation is `DELETE /access-tokens/:access_token` (base URL `https://mindcloud.scalr.io/api/iacp/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-access-token.md) for the provider-specific parameters and requirements.

