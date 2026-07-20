# Fillout Forms: List Forms

Retrieves forms from Fillout.

```
GET https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/list-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fillout Forms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/list-forms?${params}`, {
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
      "formId": "string",
      "id": 1,
      "isPublished": true,
      "name": "Ava Chen",
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formId` | string | Fillout form identifier. |
| `id` | number | Internal numeric form id. |
| `isPublished` | boolean | Whether the form is published. |
| `name` | string | Form name. |
| `tags` | array<string> | Tags assigned to the form. |

## Native endpoint

Through the native Fillout Forms API, this operation is `GET /forms` (base URL `https://api.fillout.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-forms.md) for the provider-specific parameters and requirements.

