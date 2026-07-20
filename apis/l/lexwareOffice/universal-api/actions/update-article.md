# Lexware Office: Update Article

Updates an existing article in Lexware Office.

```
PUT https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/update-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lexware Office `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/update-article" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "version": "0",
  "title": "string",
  "type": "string",
  "unitName": "Ava Chen",
  "price.leadingPrice": "NET",
  "price.taxRate": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lexwareOffice/latest/actions/update-article', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "version": "0",
    "title": "string",
    "type": "string",
    "unitName": "Ava Chen",
    "price.leadingPrice": "NET",
    "price.taxRate": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Lexware article ID. |
| `version` | number | yes | The current article version for optimistic locking. Default: `0`. |
| `title` | string | yes | The article title. |
| `description` | string | no | The article description. |
| `type` | string | yes | The article type. |
| `articleNumber` | string | no | The article number. |
| `gtin` | string | no | The article GTIN. |
| `note` | string | no | An internal note for the article. |
| `unitName` | string | yes | The sales unit name. |
| `price.leadingPrice` | string | yes | Whether Lexware should treat NET or GROSS as the leading price. Default: `NET`. |
| `price.netPrice` | number | no | The net price when the leading price is NET. |
| `price.grossPrice` | number | no | The gross price when the leading price is GROSS. |
| `price.taxRate` | number | yes | The article tax rate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "resourceUri": "string",
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
| `createdDate` | date |  |
| `id` | string |  |
| `resourceUri` | string |  |
| `updatedDate` | date |  |
| `version` | number |  |

## Native endpoint

Through the native Lexware Office API, this operation is `PUT /v1/articles/:id` (base URL `https://api.lexware.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-article.md) for the provider-specific parameters and requirements.

