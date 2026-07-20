# Qlik: Create App

Creates a new app in Qlik.

```
POST https://connect.mindcloud.co/v1/universal/qlik/latest/actions/create-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qlik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qlik/latest/actions/create-app" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "attributes.name": "Sales Dashboard"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qlik/latest/actions/create-app', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "attributes.name": "Sales Dashboard"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attributes.name` | string | yes | Name for the new Qlik app. Example: `Sales Dashboard`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "createdDate": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "name": "Ava Chen",
        "owner": "string"
      },
      "privileges": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.createdDate` | date |  |
| `attributes.id` | string |  |
| `attributes.name` | string |  |
| `attributes.owner` | string |  |
| `privileges[]` | array<string> |  |

## Native endpoint

Through the native Qlik API, this operation is `POST /api/v1/apps` (base URL `https://{{credentials.tenantHost}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-app.md) for the provider-specific parameters and requirements.

