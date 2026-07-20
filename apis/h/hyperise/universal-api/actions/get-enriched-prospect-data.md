# Hyperise: Get Enriched Prospect Data

Retrieves enriched prospect data from Hyperise by email address.

```
GET https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/get-enriched-prospect-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hyperise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/get-enriched-prospect-data?connectionId=$CONNECTION_ID&email=ava%40example.com&imageHash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com",
  "imageHash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperise/latest/actions/get-enriched-prospect-data?${params}`, {
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
| `email` | string | yes | The email address to enrich. |
| `imageHash` | string | yes | The Hyperise image template hash used for enrichment fallback. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "businessAddress": "string",
      "businessName": "Ava Chen",
      "createdAt": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "jobTitle": "string",
      "lastName": "Chen",
      "updatedAt": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessAddress` | string |  |
| `businessName` | string |  |
| `createdAt` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `jobTitle` | string |  |
| `lastName` | string |  |
| `updatedAt` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Hyperise API, this operation is `GET /data-enrichment` (base URL `https://app.hyperise.io/api/v1/regular`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-enriched-prospect-data.md) for the provider-specific parameters and requirements.

