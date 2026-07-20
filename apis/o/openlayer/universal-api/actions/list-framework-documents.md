# Openlayer: List Framework Documents

Retrieves documents for a framework in Openlayer.

```
GET https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-framework-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-framework-documents?connectionId=$CONNECTION_ID&frameworkId=29e72db4-dd2f-4331-b1c4-d13b5160a404" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "frameworkId": "29e72db4-dd2f-4331-b1c4-d13b5160a404"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/list-framework-documents?${params}`, {
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
| `frameworkId` | string | yes | Openlayer framework ID. Default: `29e72db4-dd2f-4331-b1c4-d13b5160a404`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_meta": {
        "page": 1,
        "perPage": 1,
        "totalItems": 1,
        "totalPages": 1
      },
      "items": [
        {
          "dateCreated": "string",
          "dateUpdated": "string",
          "frameworkId": "string",
          "id": "string",
          "title": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_meta.page` | number |  |
| `_meta.perPage` | number |  |
| `_meta.totalItems` | number |  |
| `_meta.totalPages` | number |  |
| `items[].dateCreated` | string |  |
| `items[].dateUpdated` | string |  |
| `items[].frameworkId` | string |  |
| `items[].id` | string |  |
| `items[].title` | string |  |

## Native endpoint

Through the native Openlayer API, this operation is `GET /frameworks/:frameworkId/documents` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-framework-documents.md) for the provider-specific parameters and requirements.

