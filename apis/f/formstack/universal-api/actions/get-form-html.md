# Formstack: Get Form HTML

Retrieves HTML markup for a form from Formstack.

```
GET https://connect.mindcloud.co/v1/universal/formstack/latest/actions/get-form-html
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formstack/latest/actions/get-form-html?connectionId=$CONNECTION_ID&formId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "formId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formstack/latest/actions/get-form-html?${params}`, {
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
| `formId` | list<number> | yes | The ID of the form. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "html": "string",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `html` | string | HTML markup for the form. |
| `id` | number | The ID of the form. |
| `name` | string | Name of the form. |

## Native endpoint

Through the native Formstack API, this operation is `GET /forms/:formId/html` (base URL `https://www.formstack.com/api/v2025`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-form-html.md) for the provider-specific parameters and requirements.

