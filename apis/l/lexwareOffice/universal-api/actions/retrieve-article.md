# Lexware Office: Retrieve Article

Retrieves an article from Lexware Office.

```
GET https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/retrieve-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lexware Office `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/retrieve-article?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/retrieve-article?${params}`, {
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
| `id` | string | yes | The Lexware article ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "articleNumber": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "gtin": "string",
      "id": "string",
      "note": "string",
      "organizationId": "string",
      "price": {
        "grossPrice": 1,
        "leadingPrice": "string",
        "netPrice": 1,
        "taxRate": 1
      },
      "title": "string",
      "type": "string",
      "unitName": "Ava Chen",
      "updatedDate": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `articleNumber` | string |  |
| `createdDate` | date |  |
| `description` | string |  |
| `gtin` | string |  |
| `id` | string |  |
| `note` | string |  |
| `organizationId` | string |  |
| `price` | object |  |
| `price.grossPrice` | number |  |
| `price.leadingPrice` | string |  |
| `price.netPrice` | number |  |
| `price.taxRate` | number |  |
| `title` | string |  |
| `type` | string |  |
| `unitName` | string |  |
| `updatedDate` | date |  |
| `version` | number |  |

## Native endpoint

Through the native Lexware Office API, this operation is `GET /v1/articles/:id` (base URL `https://api.lexware.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-article.md) for the provider-specific parameters and requirements.

