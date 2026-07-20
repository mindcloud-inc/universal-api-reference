# Jitbit Helpdesk: List Comment Templates



```
GET https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-comment-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jitbit Helpdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-comment-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-comment-templates?${params}`, {
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
      "body": "string",
      "groupId": 1,
      "groupName": "Ava Chen",
      "name": "Ava Chen",
      "templateId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string | Comment template body. |
| `groupId` | number | Template group ID when present. |
| `groupName` | string | Template group name when present. |
| `name` | string | Comment template name. |
| `templateId` | number | Comment template ID. |

## Native endpoint

Through the native Jitbit Helpdesk API, this operation is `GET /CommentTemplates` (base URL `{{credentials.helpdeskBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-comment-templates.md) for the provider-specific parameters and requirements.

