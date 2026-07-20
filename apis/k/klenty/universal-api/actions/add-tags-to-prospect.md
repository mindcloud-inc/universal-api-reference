# Klenty: Add Tags To Prospect

Adds tags to a prospect in Klenty.

```
PUT https://connect.mindcloud.co/v1/universal/klenty/latest/actions/add-tags-to-prospect
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Klenty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/klenty/latest/actions/add-tags-to-prospect" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "tags": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/klenty/latest/actions/add-tags-to-prospect', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "tags": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Prospect email address. |
| `firstName` | string | no | Prospect first name. |
| `tags` | string | yes | Pipe-delimited tag names to assign. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": {
        "email": "ava@example.com",
        "id": "string",
        "prospectOwner": "string",
        "source": "string",
        "status": true
      },
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details.email` | string |  |
| `details.id` | string |  |
| `details.prospectOwner` | string |  |
| `details.source` | string |  |
| `details.status` | boolean |  |
| `status` | boolean |  |

## Native endpoint

Through the native Klenty API, this operation is `POST /prospects` (base URL `https://api.klenty.com/apis/v1/user/{{credentials.username}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-tags-to-prospect.md) for the provider-specific parameters and requirements.

