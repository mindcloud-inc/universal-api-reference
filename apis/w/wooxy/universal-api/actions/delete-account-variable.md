# Wooxy: Delete Account Variable

Deletes an existing account variable from Wooxy.

```
DELETE https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/delete-account-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/delete-account-variable?connectionId=$CONNECTION_ID&name=stageThreeVariableAlpha" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "stageThreeVariableAlpha"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/delete-account-variable?${params}`, {
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
| `name` | string | yes | Variable name in lowerCamelCase format. Example: `stageThreeVariableAlpha`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Wooxy API returns.

## Native endpoint

Through the native Wooxy API, this operation is `POST v3/global-variables/remove` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-account-variable.md) for the provider-specific parameters and requirements.

