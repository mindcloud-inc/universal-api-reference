# Polaria: Create Brand

Creates a new brand in Polaria.

```
POST https://connect.mindcloud.co/v1/universal/polaria/latest/actions/create-brand
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Polaria `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/polaria/latest/actions/create-brand" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/polaria/latest/actions/create-brand', {
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
| `name` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiKey": "string",
      "available": true,
      "color": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "displayedImage": "string",
      "displayedName": "Ava Chen",
      "id": "string",
      "name": "Ava Chen",
      "onlineGreetings": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "windowTitle": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKey` | string |  |
| `available` | boolean |  |
| `color` | string |  |
| `createdAt` | date |  |
| `displayedImage` | string |  |
| `displayedName` | string |  |
| `id` | string |  |
| `name` | string |  |
| `onlineGreetings` | string |  |
| `updatedAt` | date |  |
| `windowTitle` | string |  |

## Native endpoint

Through the native Polaria API, this operation is `POST /widgets` (base URL `https://app.polaria.ai/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-brand.md) for the provider-specific parameters and requirements.

