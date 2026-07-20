# Qlik: Create Collection

Creates a new collection in Qlik.

```
POST https://connect.mindcloud.co/v1/universal/qlik/latest/actions/create-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qlik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qlik/latest/actions/create-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Executive dashboards",
  "type": "generic"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qlik/latest/actions/create-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Executive dashboards",
    "type": "generic"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Collection name. Example: `Executive dashboards`. |
| `type` | string | yes | Collection type. Example: `generic`. |
| `description` | string | no | Collection description. Example: `Important dashboards`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "itemCount": 1,
      "name": "Ava Chen",
      "tenantId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `itemCount` | number |  |
| `name` | string |  |
| `tenantId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Qlik API, this operation is `POST /api/v1/collections` (base URL `https://{{credentials.tenantHost}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-collection.md) for the provider-specific parameters and requirements.

