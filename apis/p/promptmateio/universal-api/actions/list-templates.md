# Promptmate.io: List Templates



```
GET https://connect.mindcloud.co/v1/universal/promptmateio/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Promptmate.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/promptmateio/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/promptmateio/latest/actions/list-templates?${params}`, {
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
      "dataFields": [
        {}
      ],
      "id": "string",
      "templateCategory": "string",
      "templateDescription": "string",
      "templateName": "Ava Chen",
      "templateType": "string",
      "templateVideo_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataFields` | array<object> | Template input field definitions. |
| `id` | string | Promptmate template ID. |
| `templateCategory` | string | Template category label. |
| `templateDescription` | string | Template description HTML. |
| `templateName` | string | Template display name. |
| `templateType` | string | Template visibility/type. |
| `templateVideo_url` | string | Optional template video URL. |

## Native endpoint

Through the native Promptmate.io API, this operation is `GET /templates` (base URL `https://api.promptmate.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

