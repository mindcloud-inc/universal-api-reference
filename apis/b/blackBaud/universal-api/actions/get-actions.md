# BlackBaud: Get Actions



```
GET https://connect.mindcloud.co/v1/universal/blackBaud/latest/actions/get-actions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlackBaud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blackBaud/latest/actions/get-actions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blackBaud/latest/actions/get-actions?${params}`, {
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
| `limit` | number | no | Maximum number of constituents to return. Example: `100`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `offset` | number | no | Number of rows to skip before returning constituents. Example: `0`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BlackBaud API returns.

## Native endpoint

Through the native BlackBaud API, this operation is `GET constituent/v1/actions` (base URL `https://api.sky.blackbaud.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-actions.md) for the provider-specific parameters and requirements.

