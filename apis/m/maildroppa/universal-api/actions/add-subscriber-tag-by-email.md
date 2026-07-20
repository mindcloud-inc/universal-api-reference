# Maildroppa: Add Subscriber Tag By Email



```
PUT https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/add-subscriber-tag-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildroppa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/add-subscriber-tag-by-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildroppa/latest/actions/add-subscriber-tag-by-email', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | Email address of the subscriber whose tag is being created or removed. |
| `tagTypeId` | string | no | UUID of the TagType that is being associated with or removed from the subscriber. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "id": "string",
      "name": "Ava Chen",
      "systemTag": true,
      "userTag": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | Technical tag category. |
| `id` | string | Unique identifier of the tag. |
| `name` | string | Name of the tag type. |
| `systemTag` | boolean | Whether the tag is system-managed. |
| `userTag` | boolean | Whether the tag is user-managed. |

## Native endpoint

Through the native Maildroppa API, this operation is `POST /subscribers/tags/by-email` (base URL `https://api.maildroppa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-subscriber-tag-by-email.md) for the provider-specific parameters and requirements.

