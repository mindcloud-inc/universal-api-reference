# Process Plan: Get Custom Data Query Result As Text Value for Process Template Field



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-custom-data-query-result-as-text-value-for-process-template-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-custom-data-query-result-as-text-value-for-process-template-field?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-custom-data-query-result-as-text-value-for-process-template-field?${params}`, {
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
| `processTemplateFieldId` | string | no | Process template field ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result_list": [
        {
          "developer_message": "string",
          "http_status_code": 1,
          "message_number": 1
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
| `result_list[].developer_message` | string |  |
| `result_list[].http_status_code` | number |  |
| `result_list[].message_number` | number |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /process_template_field/:processTemplateFieldId/custom_data_query_result/as_text_value` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-custom-data-query-result-as-text-value-for-process-template-field.md) for the provider-specific parameters and requirements.

