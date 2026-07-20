# Klenty: Get Prospect Status By ID

Retrieves prospect status from Klenty by ID.

```
GET https://connect.mindcloud.co/v1/universal/klenty/latest/actions/get-prospect-status-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Klenty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/klenty/latest/actions/get-prospect-status-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/klenty/latest/actions/get-prospect-status-by-id?${params}`, {
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
| `id` | string | yes | Klenty prospect ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cadenceStatus": "string",
      "prospectStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cadenceStatus` | string |  |
| `prospectStatus` | string |  |

## Native endpoint

Through the native Klenty API, this operation is `GET /prospects/{{id}}/status` (base URL `https://api.klenty.com/apis/v1/user/{{credentials.username}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-prospect-status-by-id.md) for the provider-specific parameters and requirements.

