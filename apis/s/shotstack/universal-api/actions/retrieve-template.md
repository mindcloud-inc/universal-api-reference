# Shotstack: Retrieve Template



```
GET https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/retrieve-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shotstack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/retrieve-template?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shotstack/latest/actions/retrieve-template?${params}`, {
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
| `id` | string | yes | The Shotstack template ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "response": {
        "id": "string",
        "name": "Ava Chen",
        "owner": "string",
        "template": {}
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Status message returned by Shotstack. |
| `response.id` | string | Template identifier. |
| `response.name` | string | Template name. |
| `response.owner` | string | Owner identifier for the template. |
| `response.template` | object | Template edit definition. |
| `success` | boolean | Whether the template retrieval succeeded. |

## Native endpoint

Through the native Shotstack API, this operation is `GET /edit/v1/templates/:id` (base URL `https://api.shotstack.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-template.md) for the provider-specific parameters and requirements.

