# Campaign Monitor: Delete Subscriber

Deletes a subscriber from a Campaign Monitor list by email address.

```
DELETE https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/delete-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Monitor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/delete-subscriber?connectionId=$CONNECTION_ID&listId=string&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string",
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/delete-subscriber?${params}`, {
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
| `listId` | string | yes | Campaign Monitor list identifier. |
| `email` | string | yes | Subscriber email address to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Empty string on success because Campaign Monitor returns HTTP 200 OK with no response body for subscriber deletes. |

## Native endpoint

Through the native Campaign Monitor API, this operation is `DELETE /subscribers/:listId.json` (base URL `https://api.createsend.com/api/v3.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-subscriber.md) for the provider-specific parameters and requirements.

