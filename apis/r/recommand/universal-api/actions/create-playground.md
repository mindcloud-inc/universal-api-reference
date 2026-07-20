# Recommand: Create Playground

Creates a new playground in Recommand.

```
POST https://connect.mindcloud.co/v1/universal/recommand/latest/actions/create-playground
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/create-playground" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recommand/latest/actions/create-playground', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Playground name |
| `usetestnetwork` | boolean | no | Whether to use the Peppol Test Network |

## Response

```json
{
  "success": true,
  "data": [
    {
      "playground": {
        "createdAt": "string",
        "id": "string",
        "isPlayground": true,
        "name": "Ava Chen",
        "teamDescription": "string",
        "updatedAt": "string",
        "useTestNetwork": true
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
| `playground` | object |  |
| `playground.createdAt` | string |  |
| `playground.id` | string |  |
| `playground.isPlayground` | boolean |  |
| `playground.name` | string |  |
| `playground.teamDescription` | string |  |
| `playground.updatedAt` | string |  |
| `playground.useTestNetwork` | boolean |  |
| `success` | boolean |  |

## Native endpoint

Through the native Recommand API, this operation is `POST /api/v1/playgrounds` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-playground.md) for the provider-specific parameters and requirements.

