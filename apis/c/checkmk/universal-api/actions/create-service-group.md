# Checkmk: Create Service Group

Creates a new service group in Checkmk.

```
POST https://connect.mindcloud.co/v1/universal/checkmk/latest/actions/create-service-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkmk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/checkmk/latest/actions/create-service-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "alias": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkmk/latest/actions/create-service-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "alias": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Service group name. |
| `alias` | string | yes | Service group display alias. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "extensions": {},
      "id": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `extensions` | object |  |
| `id` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Checkmk API, this operation is `POST /domain-types/service_group_config/collections/all` (base URL `{{credentials.apiUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-service-group.md) for the provider-specific parameters and requirements.

