# Printful: Get Mockup Task

Retrieves a Printful mockup generation task result.

```
GET https://connect.mindcloud.co/v1/universal/printful/latest/actions/get-mockup-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printful/latest/actions/get-mockup-task?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printful/latest/actions/get-mockup-task?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "mockups": [
        {}
      ],
      "status": "string",
      "task_key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `mockups` | array<object> |  |
| `status` | string |  |
| `task_key` | string |  |

## Native endpoint

Through the native Printful API, this operation is `GET /mockup-generator/task` (base URL `https://api.printful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mockup-task.md) for the provider-specific parameters and requirements.

