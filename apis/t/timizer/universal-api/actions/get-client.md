# Timizer: Get Client

Retrieves a client from Timizer.

```
GET https://connect.mindcloud.co/v1/universal/timizer/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timizer/latest/actions/get-client?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timizer/latest/actions/get-client?${params}`, {
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
| `id` | string | no | ID of the client. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "city": "string",
      "contacts": [
        {}
      ],
      "country": "string",
      "fullAddress": "string",
      "id": 1,
      "name": "Ava Chen",
      "note": "string",
      "pennylaneId": 1,
      "postalCode": "string",
      "siret": "string",
      "teamId": 1,
      "uniqueIdentifier": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `city` | string |  |
| `contacts` | array<object> |  |
| `country` | string |  |
| `fullAddress` | string |  |
| `id` | number |  |
| `name` | string |  |
| `note` | string |  |
| `pennylaneId` | number |  |
| `postalCode` | string |  |
| `siret` | string |  |
| `teamId` | number |  |
| `uniqueIdentifier` | string |  |

## Native endpoint

Through the native Timizer API, this operation is `GET /app/clients/:id` (base URL `https://api.timizer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

