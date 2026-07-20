# Feathery: List API Connector Errors



```
GET https://connect.mindcloud.co/v1/universal/feathery/latest/actions/list-api-connector-errors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feathery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feathery/latest/actions/list-api-connector-errors?connectionId=$CONNECTION_ID&form_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "form_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feathery/latest/actions/list-api-connector-errors?${params}`, {
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
| `form_id` | string | yes | The ID of the form whose API connector errors you want to inspect. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `start_time` | date | no | Only return errors after this time. |
| `end_time` | date | no | Only return errors before this time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "request": "string",
      "response": "string",
      "status_code": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | When the error was received. |
| `request` | string | The truncated request payload. |
| `response` | string | The truncated response payload. |
| `status_code` | number | The returned status code. |
| `url` | string | The endpoint URL that returned an error. |

## Native endpoint

Through the native Feathery API, this operation is `GET /api/logs/api-connector/:form_id/` (base URL `https://api.feathery.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-api-connector-errors.md) for the provider-specific parameters and requirements.

