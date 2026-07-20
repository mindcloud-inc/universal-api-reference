# Dash.app: Create Collection

Creates a new collection in Dash.app.

```
POST https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/create-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dash.app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/create-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloud Dash.app smoke test"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/create-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloud Dash.app smoke test"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the collection to create. Example: `MindCloud Dash.app smoke test`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "collaborators": [
        {}
      ],
      "creatorId": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "share": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `collaborators` | array<object> |  |
| `creatorId` | string |  |
| `dateCreated` | date |  |
| `id` | string |  |
| `name` | string |  |
| `share` | object |  |

## Native endpoint

Through the native Dash.app API, this operation is `POST /collections` (base URL `https://api-v2.dash.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-collection.md) for the provider-specific parameters and requirements.

