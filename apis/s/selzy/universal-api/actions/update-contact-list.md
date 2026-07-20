# Selzy: Update Contact List

Updates an existing contact list in Selzy.

```
PUT https://connect.mindcloud.co/v1/universal/selzy/latest/actions/update-contact-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Selzy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/selzy/latest/actions/update-contact-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": 1,
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/selzy/latest/actions/update-contact-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": 1,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | number | yes | List code from getLists or createList. |
| `title` | string | yes | Unique contact list name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `beforeSubscribeUrl` | string | no | Redirect URL shown before confirmed subscription. |
| `afterSubscribeUrl` | string | no | Redirect URL shown after successful subscription. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |

## Native endpoint

Through the native Selzy API, this operation is `POST updateList` (base URL `https://api.selzy.com/en/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-list.md) for the provider-specific parameters and requirements.

