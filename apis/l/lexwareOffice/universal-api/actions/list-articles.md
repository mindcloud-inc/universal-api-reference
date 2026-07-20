# Lexware Office: List Articles

Retrieves a list of articles from Lexware Office.

```
GET https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/list-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lexware Office `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/list-articles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/list-articles?${params}`, {
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
| `articleNumber` | string | no | Filter articles by article number. |
| `gtin` | string | no | Filter articles by GTIN. |
| `type` | string | no | Filter articles by type. |

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

Through the native Lexware Office API, this operation is `GET /v1/articles` (base URL `https://api.lexware.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-articles.md) for the provider-specific parameters and requirements.

