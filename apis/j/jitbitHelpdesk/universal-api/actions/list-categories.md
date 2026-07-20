# Jitbit Helpdesk: List Categories



```
GET https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jitbit Helpdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/list-categories?${params}`, {
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
      "categoryId": 1,
      "disabled": true,
      "forTechsOnly": true,
      "name": "Ava Chen",
      "nameWithSection": "Ava Chen",
      "section": "string",
      "sectionId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryId` | number | Category ID. |
| `disabled` | boolean | Whether the category is disabled. |
| `forTechsOnly` | boolean | Whether the category is visible only to technicians. |
| `name` | string | Category name. |
| `nameWithSection` | string | Category name including section path. |
| `section` | string | Section name when present. |
| `sectionId` | number | Section ID when present. |

## Native endpoint

Through the native Jitbit Helpdesk API, this operation is `GET /categories` (base URL `{{credentials.helpdeskBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-categories.md) for the provider-specific parameters and requirements.

