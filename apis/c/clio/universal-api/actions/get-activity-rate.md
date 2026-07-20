# Clio Manage: Get Activity Rate

Retrieves an activity rate from Clio Manage by ID.

```
GET https://connect.mindcloud.co/v1/universal/clio/latest/actions/get-activity-rate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clio Manage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clio/latest/actions/get-activity-rate?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clio/latest/actions/get-activity-rate?${params}`, {
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
| `id` | number | yes | The Clio activity rate ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "etag": "string",
      "id": 1,
      "rate": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `etag` | string |  |
| `id` | number |  |
| `rate` | number |  |

## Native endpoint

Through the native Clio Manage API, this operation is `GET /activity_rates/:id.json` (base URL `https://app.clio.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-activity-rate.md) for the provider-specific parameters and requirements.

