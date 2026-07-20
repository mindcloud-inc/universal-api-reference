# Postman: Delete Monitor

Deletes an existing monitor from Postman.

```
DELETE https://connect.mindcloud.co/v1/universal/postman/latest/actions/delete-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/postman/latest/actions/delete-monitor?connectionId=$CONNECTION_ID&monitorId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "monitorId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postman/latest/actions/delete-monitor?${params}`, {
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
| `monitorId` | string | yes | The monitor's ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "monitor": {
        "id": "string",
        "uid": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `monitor.id` | string |  |
| `monitor.uid` | string |  |

## Native endpoint

Through the native Postman API, this operation is `DELETE /monitors/:monitorId` (base URL `https://api.getpostman.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-monitor.md) for the provider-specific parameters and requirements.

