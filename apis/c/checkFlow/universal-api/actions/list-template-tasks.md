# CheckFlow: List Template Tasks



```
GET https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/list-template-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CheckFlow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/list-template-tasks?connectionId=$CONNECTION_ID&templateKey=0e7ad584-7788-4ab1-95a6-ca0a5b444cbb" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateKey": "0e7ad584-7788-4ab1-95a6-ca0a5b444cbb"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkFlow/latest/actions/list-template-tasks?${params}`, {
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
| `templateKey` | string | yes | The key of the template. Use List Templates to find the key. Example: `0e7ad584-7788-4ab1-95a6-ca0a5b444cbb`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native CheckFlow API, this operation is `GET /api/template/tasks` (base URL `https://app.checkflow.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-template-tasks.md) for the provider-specific parameters and requirements.

