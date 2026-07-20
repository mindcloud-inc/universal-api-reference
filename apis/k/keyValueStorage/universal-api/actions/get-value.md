# Key Value Storage: Get Value



```
GET https://connect.mindcloud.co/v1/universal/keyValueStorage/latest/actions/get-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Key Value Storage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keyValueStorage/latest/actions/get-value?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keyValueStorage/latest/actions/get-value?${params}`, {
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
| `namespace` | string | no |  |
| `key` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Key Value Storage API returns.

## Native endpoint

Through the native Key Value Storage API, this operation is `GET`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-value.md) for the provider-specific parameters and requirements.

