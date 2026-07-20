# Reloadify: Create Global Unsubscription

Creates a global unsubscription in Reloadify.

```
POST https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-global-unsubscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reloadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-global-unsubscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "languageId": "string",
  "global_unsubscribe.email": "ava@example.com",
  "global_unsubscribe.unsubscribed": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reloadify/latest/actions/create-global-unsubscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "languageId": "string",
    "global_unsubscribe.email": "ava@example.com",
    "global_unsubscribe.unsubscribed": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `languageId` | string | yes | Reloadify language ID. |
| `global_unsubscribe.email` | string | yes | Email to unsubscribe globally. |
| `global_unsubscribe.unsubscribed` | boolean | yes | Whether the address is unsubscribed globally. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | boolean |  |

## Native endpoint

Through the native Reloadify API, this operation is `PUT /v2/languages/:language_id/global_unsubscribes` (base URL `https://api.reloadify.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-global-unsubscription.md) for the provider-specific parameters and requirements.

