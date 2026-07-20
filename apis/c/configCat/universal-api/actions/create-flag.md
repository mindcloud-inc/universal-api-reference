# ConfigCat: Create Flag

Creates a new flag in ConfigCat.

```
POST https://connect.mindcloud.co/v1/universal/configCat/latest/actions/create-flag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ConfigCat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/configCat/latest/actions/create-flag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "configId": "string",
  "flag": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/configCat/latest/actions/create-flag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "configId": "string",
    "flag": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `configId` | string | yes | The identifier of the Config. |
| `flag` | object | yes | Raw ConfigCat flag body. Create requires key, name, and settingType. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ConfigCat API returns.

## Native endpoint

Through the native ConfigCat API, this operation is `POST /v1/configs/:configId/settings` (base URL `https://api.configcat.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-flag.md) for the provider-specific parameters and requirements.

