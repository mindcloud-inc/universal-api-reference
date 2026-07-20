# Dash.app: Get Field Option

Retrieves a field option from Dash.app by ID.

```
GET https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/get-field-option
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dash.app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/get-field-option?connectionId=$CONNECTION_ID&id=1fc6d6c3-c42d-48e2-b0db-5d680a58ca52" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1fc6d6c3-c42d-48e2-b0db-5d680a58ca52"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/get-field-option?${params}`, {
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
| `id` | string | yes | Example: `1fc6d6c3-c42d-48e2-b0db-5d680a58ca52`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "permittedActions": [
        {}
      ],
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `permittedActions` | array<object> |  |
| `result` | object |  |

## Native endpoint

Through the native Dash.app API, this operation is `GET /field-options/:id` (base URL `https://api-v2.dash.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-field-option.md) for the provider-specific parameters and requirements.

