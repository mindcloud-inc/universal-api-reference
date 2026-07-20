# Adyntel: Get Google Shopping Status

Retrieves Google Shopping search results from Adyntel by search ID.

```
GET https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/get-google-shopping-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Adyntel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/get-google-shopping-status?connectionId=$CONNECTION_ID&id=task-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "task-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/get-google-shopping-status?${params}`, {
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
| `id` | string | yes | Request ID returned by the initial Google Shopping action. Example: `task-id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ads": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ads` | array<object> |  |

## Native endpoint

Through the native Adyntel API, this operation is `POST /google_shopping_status` (base URL `https://api.adyntel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-google-shopping-status.md) for the provider-specific parameters and requirements.

