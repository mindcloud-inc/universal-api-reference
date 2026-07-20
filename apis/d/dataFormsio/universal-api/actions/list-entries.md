# DataForms.io: List Entries

Retrieves entries from DataForms.io.

```
GET https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/list-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForms.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/list-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/list-entries?${params}`, {
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
| `limit` | number | no | Limit the number of entries returned. Maximum 50. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "answers": [
            {
              "fieldId": "string",
              "label": "string",
              "type": "string",
              "value": "string"
            }
          ],
          "count": 1,
          "createdAt": "string",
          "dataFormId": "string",
          "id": "string",
          "submitted": true,
          "submittedAt": "string",
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
| `data[].answers[].fieldId` | string |  |
| `data[].answers[].label` | string |  |
| `data[].answers[].type` | string |  |
| `data[].answers[].value` | string |  |
| `data[].count` | number |  |
| `data[].createdAt` | string |  |
| `data[].dataFormId` | string |  |
| `data[].id` | string |  |
| `data[].submitted` | boolean |  |
| `data[].submittedAt` | string |  |
| `data[].updatedAt` | string |  |
| `meta.currentPage` | number |  |
| `meta.lastPage` | number |  |
| `meta.perPage` | number |  |
| `meta.total` | number |  |

## Native endpoint

Through the native DataForms.io API, this operation is `GET /entries` (base URL `https://api.dataforms.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-entries.md) for the provider-specific parameters and requirements.

