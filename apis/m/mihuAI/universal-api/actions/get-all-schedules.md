# Mihu AI: Get All Schedules



```
GET https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/get-all-schedules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mihu AI `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/get-all-schedules?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/get-all-schedules?${params}`, {
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
| `availabilityTypeUuid` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availabilityTypeUuid": "string",
      "color": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availabilityTypeUuid` | string |  |
| `color` | string |  |
| `createdAt` | date |  |
| `name` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Mihu AI API, this operation is `GET /api/v1/schedules` (base URL `https://{{credentials.subdomain}}.mindhunters.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-schedules.md) for the provider-specific parameters and requirements.

