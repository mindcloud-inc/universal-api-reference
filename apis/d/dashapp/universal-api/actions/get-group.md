# Dash.app: Get Group

Retrieves a group from Dash.app by ID.

```
GET https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/get-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dash.app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/get-group?connectionId=$CONNECTION_ID&id=ba24de5f-1234-5678-90ab-abcdef123456" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "ba24de5f-1234-5678-90ab-abcdef123456"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/get-group?${params}`, {
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
| `id` | string | yes | The Dash group ID. Example: `ba24de5f-1234-5678-90ab-abcdef123456`. |

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

Through the native Dash.app API, this operation is `GET /groups/:id` (base URL `https://api-v2.dash.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group.md) for the provider-specific parameters and requirements.

