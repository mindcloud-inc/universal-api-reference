# Whop: Retrieve Forum

Retrieves forum details from the Whop platform.

```
GET https://connect.mindcloud.co/v1/universal/whop/latest/actions/retrieve-forum
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whop/latest/actions/retrieve-forum?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whop/latest/actions/retrieve-forum?${params}`, {
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
| `id` | string | yes | The unique identifier of the forum. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emailNotificationPreference": "ava@example.com",
      "experience": {
        "id": "string",
        "name": "Ava Chen"
      },
      "id": "string",
      "whoCanComment": "string",
      "whoCanPost": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailNotificationPreference` | string |  |
| `experience` | object |  |
| `experience.id` | string |  |
| `experience.name` | string |  |
| `id` | string |  |
| `whoCanComment` | string |  |
| `whoCanPost` | string |  |

## Native endpoint

Through the native Whop API, this operation is `GET /api/v1/forums/:id` (base URL `https://api.whop.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-forum.md) for the provider-specific parameters and requirements.

