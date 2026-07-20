# Nyckel: Create Label

Creates a new label in Nyckel.

```
POST https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/create-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nyckel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/create-label" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "functionId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/create-label', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "functionId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `functionId` | string | yes | Nyckel function identifier. |
| `name` | string | yes | Label name. |
| `description` | string | no | Optional label description. |
| `metadata` | object | no | Optional label metadata object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Nyckel API, this operation is `POST /functions/:functionId/labels` (base URL `https://www.nyckel.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-label.md) for the provider-specific parameters and requirements.

