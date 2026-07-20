# Recommand: Create Label

Creates a new label in Recommand.

```
POST https://connect.mindcloud.co/v1/universal/recommand/latest/actions/create-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/create-label" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "colorhex": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recommand/latest/actions/create-label', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "colorhex": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `colorhex` | string | yes | colorHex body field. |
| `externalid` | string | no | externalId body field. |
| `name` | string | yes | name body field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "label": {
        "colorHex": "string",
        "createdAt": "string",
        "externalId": "string",
        "id": "string",
        "name": "Ava Chen",
        "teamId": "string",
        "updatedAt": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `label` | object |  |
| `label.colorHex` | string |  |
| `label.createdAt` | string |  |
| `label.externalId` | string |  |
| `label.id` | string |  |
| `label.name` | string |  |
| `label.teamId` | string |  |
| `label.updatedAt` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Recommand API, this operation is `POST /api/v1/labels` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-label.md) for the provider-specific parameters and requirements.

