# Persona: Remove Account Tag



```
PUT https://connect.mindcloud.co/v1/universal/persona/latest/actions/remove-account-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Persona `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/persona/latest/actions/remove-account-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "act_123",
  "tagName": "mindcloud-tag-a"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/persona/latest/actions/remove-account-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "act_123",
    "tagName": "mindcloud-tag-a"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | Account ID Example: `act_123`. |
| `tagName` | string | yes | Tag Name Example: `mindcloud-tag-a`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object |  |
| `id` | string |  |
| `relationships` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Persona API, this operation is `POST /accounts/[:account-id]/remove-tag` (base URL `https://api.withpersona.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-account-tag.md) for the provider-specific parameters and requirements.

