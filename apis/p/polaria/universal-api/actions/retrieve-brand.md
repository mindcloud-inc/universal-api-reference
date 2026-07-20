# Polaria: Retrieve Brand

Retrieves a brand from Polaria by API key.

```
GET https://connect.mindcloud.co/v1/universal/polaria/latest/actions/retrieve-brand
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Polaria `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/polaria/latest/actions/retrieve-brand?connectionId=$CONNECTION_ID&apiKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "apiKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/polaria/latest/actions/retrieve-brand?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `apiKey` | string | yes | The Polaria widget API key for the target brand. |

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

Through the native Polaria API, this operation is `GET /widgets/[:api_key]` (base URL `https://app.polaria.ai/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-brand.md) for the provider-specific parameters and requirements.

