# DataForms.io: List Templates

Retrieves templates from DataForms.io.

```
GET https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForms.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/list-templates?${params}`, {
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
| `search` | string | no | Filter templates by search term. |
| `limit` | number | no | Limit the number of templates returned. Maximum 50. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "acronym": "string",
          "confirmSubmit": true,
          "createdAt": "string",
          "description": "string",
          "id": "string",
          "layout": "string",
          "name": "Ava Chen",
          "redirectUrl": "https://example.com",
          "showHeader": true,
          "updatedAt": "string"
        }
      ],
      "meta": {
        "currentPage": 1,
        "lastPage": 1,
        "perPage": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].acronym` | string |  |
| `data[].confirmSubmit` | boolean |  |
| `data[].createdAt` | string |  |
| `data[].description` | string |  |
| `data[].id` | string |  |
| `data[].layout` | string |  |
| `data[].name` | string |  |
| `data[].redirectUrl` | string |  |
| `data[].showHeader` | boolean |  |
| `data[].updatedAt` | string |  |
| `meta.currentPage` | number |  |
| `meta.lastPage` | number |  |
| `meta.perPage` | number |  |
| `meta.total` | number |  |

## Native endpoint

Through the native DataForms.io API, this operation is `GET /templates` (base URL `https://api.dataforms.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

