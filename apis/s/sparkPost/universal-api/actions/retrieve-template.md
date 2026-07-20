# SparkPost: Retrieve Template



```
GET https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/retrieve-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparkPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/retrieve-template?connectionId=$CONNECTION_ID&id=my-first-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "my-first-email"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/retrieve-template?${params}`, {
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
| `draft` | boolean | no | Whether to retrieve the draft version. |
| `id` | string | yes | Template identifier. Default: `my-first-email`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": {},
      "description": "string",
      "hasDraft": true,
      "hasPublished": true,
      "id": "string",
      "lastUpdateTime": "string",
      "name": "Ava Chen",
      "options": {},
      "published": true,
      "sharedWithSubaccounts": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | object |  |
| `description` | string |  |
| `hasDraft` | boolean |  |
| `hasPublished` | boolean |  |
| `id` | string |  |
| `lastUpdateTime` | string |  |
| `name` | string |  |
| `options` | object |  |
| `published` | boolean |  |
| `sharedWithSubaccounts` | boolean |  |

## Native endpoint

Through the native SparkPost API, this operation is `GET /templates/:id` (base URL `https://api.sparkpost.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-template.md) for the provider-specific parameters and requirements.

