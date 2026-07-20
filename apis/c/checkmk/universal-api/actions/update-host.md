# Checkmk: Update Host

Updates an existing host in Checkmk.

```
PUT https://connect.mindcloud.co/v1/universal/checkmk/latest/actions/update-host
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkmk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/checkmk/latest/actions/update-host" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hostName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkmk/latest/actions/update-host', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hostName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hostName` | string | yes | Checkmk host name. |
| `updateAttributes` | object | no | Attributes to update. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `removeAttributes[]` | array<string> | no | Attribute names to remove. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "extensions": {},
      "id": "string",
      "links": [
        {}
      ],
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
| `links` | array<object> |  |
| `title` | string |  |

## Native endpoint

Through the native Checkmk API, this operation is `PUT /objects/host_config/{host_name}` (base URL `{{credentials.apiUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-host.md) for the provider-specific parameters and requirements.

