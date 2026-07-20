# Bannertize: Retrieve Set

Retrieves a generated set instance from Bannertize.

```
GET https://connect.mindcloud.co/v1/universal/bannertize/latest/actions/retrieve-set
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bannertize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bannertize/latest/actions/retrieve-set?connectionId=$CONNECTION_ID&set_uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "set_uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bannertize/latest/actions/retrieve-set?${params}`, {
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
| `set_uid` | string | yes | The Bannertize set render UID to retrieve. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bannertize API returns.

## Native endpoint

Through the native Bannertize API, this operation is `GET set/:set_uid` (base URL `https://api.bannertize.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-set.md) for the provider-specific parameters and requirements.

