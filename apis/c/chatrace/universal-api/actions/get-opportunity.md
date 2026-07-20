# Chatrace: Get Opportunity

Retrieves an opportunity record from Chatrace.

```
GET https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/get-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatrace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/get-opportunity?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatrace/latest/actions/get-opportunity?${params}`, {
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
      "contact_id": 1,
      "description": "string",
      "id": 1,
      "priority": "string",
      "status": "string",
      "title": "string",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact_id` | number |  |
| `description` | string |  |
| `id` | number |  |
| `priority` | string |  |
| `status` | string |  |
| `title` | string |  |
| `value` | number |  |

## Native endpoint

Through the native Chatrace API, this operation is `GET /pipelines/:pipeline_id/opportunities/:opportunity_id` (base URL `https://api.chatrace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-opportunity.md) for the provider-specific parameters and requirements.

