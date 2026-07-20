# Certifier: Get Group

Retrieves detailed group information from Certifier.

```
GET https://connect.mindcloud.co/v1/universal/certifier/latest/actions/get-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Certifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/certifier/latest/actions/get-group?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/certifier/latest/actions/get-group?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "badgeDesignId": "string",
      "certificateDesignId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "learningEventUrl": "https://example.com",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `badgeDesignId` | string |  |
| `certificateDesignId` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `learningEventUrl` | string |  |
| `name` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Certifier API, this operation is `GET /groups/:id` (base URL `https://api.certifier.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-group.md) for the provider-specific parameters and requirements.

