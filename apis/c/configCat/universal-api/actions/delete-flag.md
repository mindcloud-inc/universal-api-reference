# ConfigCat: Delete Flag

Deletes an existing flag from ConfigCat.

```
DELETE https://connect.mindcloud.co/v1/universal/configCat/latest/actions/delete-flag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ConfigCat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/configCat/latest/actions/delete-flag?connectionId=$CONNECTION_ID&settingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "settingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/configCat/latest/actions/delete-flag?${params}`, {
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
| `settingId` | string | yes | The identifier of the Flag. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ConfigCat API returns.

## Native endpoint

Through the native ConfigCat API, this operation is `DELETE /v1/settings/:settingId` (base URL `https://api.configcat.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-flag.md) for the provider-specific parameters and requirements.

