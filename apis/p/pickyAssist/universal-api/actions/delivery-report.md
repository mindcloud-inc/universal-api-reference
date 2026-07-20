# Picky Assist: Delivery Report



```
GET https://connect.mindcloud.co/v1/universal/pickyAssist/latest/actions/delivery-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Picky Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pickyAssist/latest/actions/delivery-report?connectionId=$CONNECTION_ID&push_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "push_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pickyAssist/latest/actions/delivery-report?${params}`, {
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
| `push_id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "application": "string",
      "data": [
        {
          "error_code": "string",
          "msg_id": "string",
          "number": "string",
          "status": "string"
        }
      ],
      "message_type": "string",
      "project_id": "string",
      "push_id": 1,
      "time": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `application` | string |  |
| `data[].error_code` | string |  |
| `data[].msg_id` | string |  |
| `data[].number` | string |  |
| `data[].status` | string |  |
| `message_type` | string |  |
| `project_id` | string |  |
| `push_id` | number |  |
| `time` | string |  |

## Native endpoint

Through the native Picky Assist API, this operation is `POST /delivery-report` (base URL `https://app.pickyassist.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delivery-report.md) for the provider-specific parameters and requirements.

