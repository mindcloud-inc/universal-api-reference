# Instafill: Search Forms



```
GET https://connect.mindcloud.co/v1/universal/instafill/latest/actions/search-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instafill `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instafill/latest/actions/search-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instafill/latest/actions/search-forms?${params}`, {
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
| `q` | string | no |  |
| `limit` | number | no |  |
| `offset` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "forms": [
        [
          {}
        ]
      ],
      "id": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `forms[]` | array<object> |  |
| `forms[].batch_id` | string |  |
| `forms[].file_name` | string |  |
| `forms[].form_id` | string |  |
| `forms[].form_url` | string |  |
| `forms[].processed` | boolean |  |
| `id` | string |  |
| `object` | string |  |

## Native endpoint

Through the native Instafill API, this operation is `GET /v1/forms/search` (base URL `https://api.instafill.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-forms.md) for the provider-specific parameters and requirements.

