# Presenton: Get Standard Template Example



```
GET https://connect.mindcloud.co/v1/universal/presenton/latest/actions/get-standard-template-example
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Presenton `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/presenton/latest/actions/get-standard-template-example?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/presenton/latest/actions/get-standard-template-example?${params}`, {
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
| `id` | string | yes | The standard template ID to use for the example. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "slides": [
        [
          {}
        ]
      ],
      "standardTemplate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `slides[]` | array<object> |  |
| `slides[].content.description` | string |  |
| `slides[].content.title` | string |  |
| `slides[].layout` | string |  |
| `standardTemplate` | string |  |

## Native endpoint

Through the native Presenton API, this operation is `GET /api/v3/standard-template/:id/example` (base URL `https://api.presenton.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-standard-template-example.md) for the provider-specific parameters and requirements.

