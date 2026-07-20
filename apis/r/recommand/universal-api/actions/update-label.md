# Recommand: Update Label

Updates an existing label in Recommand.

```
PUT https://connect.mindcloud.co/v1/universal/recommand/latest/actions/update-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recommand `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/recommand/latest/actions/update-label" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "labelid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recommand/latest/actions/update-label', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "labelid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `colorhex` | string | no | colorHex body field. |
| `externalid` | string | no | externalId body field. |
| `labelid` | string | yes | labelId parameter. |
| `name` | string | no | name body field. |

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

Through the native Recommand API, this operation is `PUT /api/v1/labels/:labelId` (base URL `https://app.recommand.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-label.md) for the provider-specific parameters and requirements.

