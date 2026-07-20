# Lark Drive: Check File Task



```
GET https://connect.mindcloud.co/v1/universal/larkDrive/latest/actions/check-file-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lark Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/larkDrive/latest/actions/check-file-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/larkDrive/latest/actions/check-file-task?${params}`, {
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
| `taskId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "status": "string"
      },
      "msg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data.status` | string |  |
| `msg` | string |  |

## Native endpoint

Through the native Lark Drive API, this operation is `GET /drive/v1/files/task_check` (base URL `https://open.larksuite.com/open-apis`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-file-task.md) for the provider-specific parameters and requirements.

