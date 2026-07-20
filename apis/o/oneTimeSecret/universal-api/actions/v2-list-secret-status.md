# One-Time Secret: List Secret Status

Retrieves statuses for multiple secrets in One-Time Secret.

```
GET https://connect.mindcloud.co/v1/universal/oneTimeSecret/latest/actions/v2-list-secret-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a One-Time Secret `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneTimeSecret/latest/actions/v2-list-secret-status?connectionId=$CONNECTION_ID&identifiers%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifiers[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneTimeSecret/latest/actions/v2-list-secret-status?${params}`, {
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
| `identifiers[]` | array<string> | yes | Secret identifiers to check status for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "details": {},
      "records": [
        {}
      ],
      "shrimp": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of status records returned. |
| `details` | object | Batch status details returned by One-Time Secret. |
| `records` | array<object> | Secret status records. |
| `shrimp` | string | Provider response marker when returned. |
| `user_id` | string | Authenticated user identifier when returned. |

## Native endpoint

Through the native One-Time Secret API, this operation is `POST /api/v2/secret/status` (base URL `https://us.onetimesecret.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v2-list-secret-status.md) for the provider-specific parameters and requirements.

