# ConfigCat: Update Config

Updates an existing config in ConfigCat.

```
PUT https://connect.mindcloud.co/v1/universal/configCat/latest/actions/update-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ConfigCat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/configCat/latest/actions/update-config" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "configId": "string",
  "config": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/configCat/latest/actions/update-config', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "configId": "string",
    "config": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `configId` | string | yes | The identifier of the Config. |
| `config` | object | yes | Raw ConfigCat config body. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ConfigCat API returns.

## Native endpoint

Through the native ConfigCat API, this operation is `PUT /v1/configs/:configId` (base URL `https://api.configcat.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-config.md) for the provider-specific parameters and requirements.

