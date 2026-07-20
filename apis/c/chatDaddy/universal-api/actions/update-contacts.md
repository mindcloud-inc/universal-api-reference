# ChatDaddy: Update Contacts

Updates one or more existing contacts in ChatDaddy.

```
PUT https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/update-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatDaddy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/update-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "patch": {
    "name": "Updated contact"
  }
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatDaddy/latest/actions/update-contacts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "patch": {"name":"Updated contact"}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `patch` | object | yes | Patch instructions for updating contacts. Default: `{"name":"Updated contact"}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true,
      "updated": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the contact update request completed successfully. |
| `updated` | number | How many contacts were updated by the patch. |

## Native endpoint

Through the native ChatDaddy API, this operation is `PATCH /contacts` (base URL `https://api.chatdaddy.tech/im`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contacts.md) for the provider-specific parameters and requirements.

