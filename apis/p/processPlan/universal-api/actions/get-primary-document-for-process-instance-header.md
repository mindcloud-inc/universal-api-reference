# Process Plan: Get Primary Document for Process Instance Header



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-primary-document-for-process-instance-header
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-primary-document-for-process-instance-header?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/get-primary-document-for-process-instance-header?${params}`, {
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
| `processInstanceHeaderId` | string | no | Process instance header ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result_list": [
        {
          "http_status_code": 1,
          "message_number": 1,
          "user_message": "string"
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
| `result_list[].http_status_code` | number |  |
| `result_list[].message_number` | number |  |
| `result_list[].user_message` | string |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /process_instance_header/:processInstanceHeaderId/primary_document` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-primary-document-for-process-instance-header.md) for the provider-specific parameters and requirements.

