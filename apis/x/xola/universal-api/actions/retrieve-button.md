# Xola: Retrieve Button

Retrieves a button from Xola by ID.

```
GET https://connect.mindcloud.co/v1/universal/xola/latest/actions/retrieve-button
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xola `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xola/latest/actions/retrieve-button?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xola/latest/actions/retrieve-button?${params}`, {
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
| `id` | string | yes | Button identifier from Xola. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "experience": {
        "id": "string"
      },
      "id": "string",
      "name": "Ava Chen",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `experience.id` | string | Associated experience identifier. |
| `id` | string | Button identifier. |
| `name` | string | Button name. |
| `object` | string | Xola object type. |

## Native endpoint

Through the native Xola API, this operation is `GET /buttons/{id}` (base URL `https://sandbox.xola.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-button.md) for the provider-specific parameters and requirements.

