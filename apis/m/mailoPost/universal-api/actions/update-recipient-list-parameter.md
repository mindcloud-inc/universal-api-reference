# MailoPost: Update Recipient List Parameter

Updates an existing recipient list parameter in MailoPost.

```
PUT https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/update-recipient-list-parameter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailoPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/update-recipient-list-parameter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/update-recipient-list-parameter', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | string | yes | MailoPost recipient list identifier. |
| `id` | string | yes | MailoPost recipient list parameter identifier. |
| `title` | string | no | Recipient list parameter title. |
| `kind` | string | no | Recipient list parameter kind. Example: `string`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "kind": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `kind` | string |  |
| `title` | string |  |

## Native endpoint

Through the native MailoPost API, this operation is `PATCH /email/lists/:list-id/parameters/:id` (base URL `https://api.mailopost.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-recipient-list-parameter.md) for the provider-specific parameters and requirements.

