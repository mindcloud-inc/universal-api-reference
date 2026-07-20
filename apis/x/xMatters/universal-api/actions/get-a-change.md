# xMatters: Get a change

Retrieves a change from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-change
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-change?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-a-change?${params}`, {
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
| `changeId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "changedAt": "2026-05-07T12:00:00.000Z",
      "changedBy": "string",
      "changeType": "string",
      "id": "string",
      "service": {
        "id": "string",
        "links": {
          "self": "https://example.com"
        },
        "recipientType": "string",
        "targetName": "Ava Chen"
      },
      "source": "string",
      "summary": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changedAt` | date |  |
| `changedBy` | string |  |
| `changeType` | string |  |
| `id` | string |  |
| `service.id` | string |  |
| `service.links.self` | string |  |
| `service.recipientType` | string |  |
| `service.targetName` | string |  |
| `source` | string |  |
| `summary` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `GET changes/{changeId}` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-change.md) for the provider-specific parameters and requirements.

