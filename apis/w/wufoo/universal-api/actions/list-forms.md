# Wufoo: List Forms

Retrieves forms from Wufoo.

```
GET https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/list-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wufoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/list-forms?${params}`, {
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
      "dateCreated": "string",
      "dateUpdated": "string",
      "description": "string",
      "email": "ava@example.com",
      "endDate": "string",
      "entryLimit": "string",
      "hash": "string",
      "isPublic": "string",
      "language": "string",
      "linkEntries": "https://example.com",
      "linkEntriesCount": "https://example.com",
      "linkFields": "https://example.com",
      "name": "Ava Chen",
      "redirectMessage": "string",
      "startDate": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreated` | string | Form creation timestamp. |
| `dateUpdated` | string | Form update timestamp. |
| `description` | string | Form description text. |
| `email` | string | Notification email configured on the form. |
| `endDate` | string | Form end date and time. |
| `entryLimit` | string | Configured entry limit. |
| `hash` | string | Wufoo form hash identifier. |
| `isPublic` | string | Wufoo public visibility flag. |
| `language` | string | Form language. |
| `linkEntries` | string | API URL for the form entries. |
| `linkEntriesCount` | string | API URL for the form entry count. |
| `linkFields` | string | API URL for the form fields. |
| `name` | string | Wufoo form name. |
| `redirectMessage` | string | Success message shown after form submission. |
| `startDate` | string | Form start date and time. |
| `url` | string | Wufoo form URL slug. |

## Native endpoint

Through the native Wufoo API, this operation is `GET /forms.json` (base URL `https://{{credentials.subdomain}}.wufoo.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-forms.md) for the provider-specific parameters and requirements.

