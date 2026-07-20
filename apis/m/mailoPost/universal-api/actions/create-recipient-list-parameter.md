# MailoPost: Create Recipient List Parameter

Creates a new recipient list parameter in MailoPost.

```
POST https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/create-recipient-list-parameter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailoPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/create-recipient-list-parameter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "title": "string",
  "kind": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/create-recipient-list-parameter', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "title": "string",
    "kind": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | MailoPost recipient list identifier. |
| `title` | string | yes | Recipient list parameter title. |
| `kind` | string | yes | Recipient list parameter kind. Example: `string`. |

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

Through the native MailoPost API, this operation is `POST /email/lists/:id/parameters` (base URL `https://api.mailopost.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-recipient-list-parameter.md) for the provider-specific parameters and requirements.

