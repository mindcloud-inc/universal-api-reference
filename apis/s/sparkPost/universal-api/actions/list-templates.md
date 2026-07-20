# SparkPost: List Templates



```
GET https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparkPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/list-templates?${params}`, {
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
| `draft` | boolean | no | Whether to list draft versions instead of published templates. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "hasDraft": true,
      "hasPublished": true,
      "id": "string",
      "lastUpdateTime": "string",
      "name": "Ava Chen",
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
| `description` | string |  |
| `hasDraft` | boolean |  |
| `hasPublished` | boolean |  |
| `id` | string |  |
| `lastUpdateTime` | string |  |
| `name` | string |  |
| `published` | boolean |  |
| `sharedWithSubaccounts` | boolean |  |

## Native endpoint

Through the native SparkPost API, this operation is `GET /templates` (base URL `https://api.sparkpost.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

