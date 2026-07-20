# Unbounce: List Page Form Fields

Retrieves form fields across all variants of an Unbounce page.

```
GET https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/list-page-form-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unbounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/list-page-form-fields?connectionId=$CONNECTION_ID&page_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "page_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unbounce/latest/actions/list-page-form-fields?${params}`, {
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
| `page_id` | string | yes | Unbounce page ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "formFields": [
        {}
      ],
      "metadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formFields` | array<object> |  |
| `metadata` | object |  |

## Native endpoint

Through the native Unbounce API, this operation is `GET /pages/:page_id/form_fields` (base URL `https://api.unbounce.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-page-form-fields.md) for the provider-specific parameters and requirements.

