# DataForms.io: Get Entry

Retrieves an entry from DataForms.io.

```
GET https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/get-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForms.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/get-entry?connectionId=$CONNECTION_ID&entryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataFormsio/latest/actions/get-entry?${params}`, {
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
| `entryId` | string | yes | The DataForms.io entry identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.answers[].fieldId` | string |  |
| `data.answers[].label` | string |  |
| `data.answers[].type` | string |  |
| `data.answers[].value` | string |  |
| `data.count` | number |  |
| `data.createdAt` | string |  |
| `data.dataFormId` | string |  |
| `data.id` | string |  |
| `data.submitted` | boolean |  |
| `data.submittedAt` | string |  |
| `data.updatedAt` | string |  |

## Native endpoint

Through the native DataForms.io API, this operation is `GET /entries/{entry_id}` (base URL `https://api.dataforms.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-entry.md) for the provider-specific parameters and requirements.

