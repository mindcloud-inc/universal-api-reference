# Zixflow: Get List Entry By ID

Retrieves a list entry from Zixflow.

```
GET https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/get-list-entry-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zixflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/get-list-entry-by-id?connectionId=$CONNECTION_ID&listId=string&entryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string",
  "entryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zixflow/latest/actions/get-list-entry-by-id?${params}`, {
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
| `listId` | string | yes | List identifier. |
| `entryId` | string | yes | List entry identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | List entry payload returned by Zixflow. |
| `message` | string | Provider success or error message. |
| `status` | boolean | Whether the list-entry lookup succeeded. |

## Native endpoint

Through the native Zixflow API, this operation is `GET /list-entries/:listId/:entryId` (base URL `https://api.zixflow.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list-entry-by-id.md) for the provider-specific parameters and requirements.

