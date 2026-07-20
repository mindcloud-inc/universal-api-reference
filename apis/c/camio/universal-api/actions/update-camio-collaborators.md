# Camio: Update Camio Collaborators

Updates Camio collaborators in Camio.

```
PUT https://connect.mindcloud.co/v1/universal/camio/latest/actions/update-camio-collaborators
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Camio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/camio/latest/actions/update-camio-collaborators" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "collaborators": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/camio/latest/actions/update-camio-collaborators', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "collaborators": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Camio id to update. |
| `collaborators` | object | yes | A collaborators object that restricts Camio access. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collaborators": {},
      "creator": {},
      "dateCreated": "string",
      "id": "string",
      "name": "Ava Chen",
      "owner": {},
      "query": {},
      "type": "string",
      "viewToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collaborators` | object | The updated collaborator restrictions. |
| `creator` | object | The creator object. |
| `dateCreated` | string | The Camio creation timestamp. |
| `id` | string | The Camio id. |
| `name` | string | The Camio name. |
| `owner` | object | The owner object. |
| `query` | object | The Camio query object. |
| `type` | string | The Camio type. |
| `viewToken` | string | The Camio view token. |

## Native endpoint

Through the native Camio API, this operation is `POST /users/me/camios` (base URL `https://camio.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-camio-collaborators.md) for the provider-specific parameters and requirements.

