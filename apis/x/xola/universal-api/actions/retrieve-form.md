# Xola: Retrieve Form

Retrieves a form from Xola by ID.

```
GET https://connect.mindcloud.co/v1/universal/xola/latest/actions/retrieve-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xola `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xola/latest/actions/retrieve-form?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xola/latest/actions/retrieve-form?${params}`, {
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
| `id` | string | yes | Form identifier from Xola. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "questions": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Form identifier. |
| `name` | string | Form name. |
| `object` | string | Xola object type. |
| `questions[]` | array<object> | Questions included in the form. |

## Native endpoint

Through the native Xola API, this operation is `GET /forms/{id}` (base URL `https://sandbox.xola.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-form.md) for the provider-specific parameters and requirements.

