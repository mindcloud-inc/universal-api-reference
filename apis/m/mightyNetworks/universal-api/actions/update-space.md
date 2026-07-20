# Mighty Networks: Update Space

Updates an existing space in Mighty Networks.

```
PUT https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/update-space
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mighty Networks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/update-space" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "networkId": "{{credentials.networkId}}",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mightyNetworks/latest/actions/update-space', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "networkId": "{{credentials.networkId}}",
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `networkId` | string | yes | Network ID. Default: `{{credentials.networkId}}`. |
| `id` | number | yes | Space ID. |
| `name` | string | no | Updated space name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | number | no | Collection ID for the space. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collectionId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collectionId` | number |  |
| `createdAt` | date |  |
| `id` | number |  |
| `name` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Mighty Networks API, this operation is `PATCH /networks/:network_id/spaces/:id` (base URL `https://api.mn.co/admin/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-space.md) for the provider-specific parameters and requirements.

