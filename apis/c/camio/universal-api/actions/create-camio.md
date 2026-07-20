# Camio: Create Camio

Creates a Camio in Camio.

```
POST https://connect.mindcloud.co/v1/universal/camio/latest/actions/create-camio
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Camio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/camio/latest/actions/create-camio" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/camio/latest/actions/create-camio', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Optional name for the Camio link. |
| `query` | object | yes | The Camio query object, for example `{ "text": "today 6am to 7am apps@mindcloud.co" }`. |
| `type` | string | no | Optional Camio type, usually `private` or `public`. Default: `private`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creator": {},
      "dateCreated": "string",
      "id": "string",
      "message": {},
      "name": "Ava Chen",
      "owner": {},
      "query": {},
      "type": "string",
      "url": "https://example.com",
      "viewToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creator` | object | The creator object. |
| `dateCreated` | string | The Camio creation timestamp. |
| `id` | string | The Camio id. |
| `message` | object | Share-message metadata returned by Camio. |
| `name` | string | The Camio name. |
| `owner` | object | The owner object. |
| `query` | object | The Camio query object. |
| `type` | string | The Camio type. |
| `url` | string | The Camio app URL. |
| `viewToken` | string | The Camio view token. |

## Native endpoint

Through the native Camio API, this operation is `PUT /users/me/camios` (base URL `https://camio.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-camio.md) for the provider-specific parameters and requirements.

