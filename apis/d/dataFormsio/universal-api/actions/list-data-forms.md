# DataForms.io: List Data Forms

Retrieves data forms from DataForms.io.

```
GET https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/list-data-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForms.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/list-data-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/list-data-forms?${params}`, {
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
| `search` | string | no | Filter data forms by search term. |
| `limit` | number | no | Limit the number of forms returned. Maximum 50. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "allowMultipleSubmissions": true,
          "createdAt": "string",
          "headline": "string",
          "id": "string",
          "lockAfterSubmission": true,
          "redirectUrl": "https://example.com",
          "templateId": "string",
          "type": "string",
          "updatedAt": "string",
          "url": "https://example.com"
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
| `data[].allowMultipleSubmissions` | boolean |  |
| `data[].createdAt` | string |  |
| `data[].headline` | string |  |
| `data[].id` | string |  |
| `data[].lockAfterSubmission` | boolean |  |
| `data[].redirectUrl` | string |  |
| `data[].templateId` | string |  |
| `data[].type` | string |  |
| `data[].updatedAt` | string |  |
| `data[].url` | string |  |
| `meta.currentPage` | number |  |
| `meta.lastPage` | number |  |
| `meta.perPage` | number |  |
| `meta.total` | number |  |

## Native endpoint

Through the native DataForms.io API, this operation is `GET /dataforms` (base URL `https://api.dataforms.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-data-forms.md) for the provider-specific parameters and requirements.

