# Mixpanel: Create Alias

Creates a user identity alias in Mixpanel.

```
POST https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/create-alias
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mixpanel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/create-alias" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "distinctId": "string",
  "alias": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/create-alias', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "distinctId": "string",
    "alias": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `distinctId` | string | yes | Existing distinct ID that should gain a new alias. |
| `alias` | string | yes | New alias that Mixpanel should interpret as the existing distinct ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `strict` | string | no | When 1, Mixpanel validates the alias payload and returns per-record validation errors. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Primitive success or failure response returned by Mixpanel for the alias request. |

## Native endpoint

Through the native Mixpanel API, this operation is `POST https://api.mixpanel.com/track` (base URL `https://mixpanel.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-alias.md) for the provider-specific parameters and requirements.

