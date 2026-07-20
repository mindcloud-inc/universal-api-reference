# Camio: List Camios

Retrieves Camios from Camio.

```
GET https://connect.mindcloud.co/v1/universal/camio/latest/actions/list-camios
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Camio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/camio/latest/actions/list-camios?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/camio/latest/actions/list-camios?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
| `collaborators` | object | Collaborator restrictions when present. |
| `creator` | object | The creator object. |
| `dateCreated` | string | The Camio creation timestamp. |
| `id` | string | The Camio id. |
| `name` | string | The Camio name. |
| `owner` | object | The owner object. |
| `query` | object | The Camio query object. |
| `type` | string | The Camio type. |
| `viewToken` | string | The Camio view token. |

## Native endpoint

Through the native Camio API, this operation is `GET /users/me/camios` (base URL `https://camio.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-camios.md) for the provider-specific parameters and requirements.

