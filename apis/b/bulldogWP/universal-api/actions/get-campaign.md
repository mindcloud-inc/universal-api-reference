# Bulldog-WP: Get campaign

Retrieves a campaign from Bulldog-WP.

```
GET https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bulldog-WP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-campaign?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-campaign?${params}`, {
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
| `campaignId` | string | yes | Campaign ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canceledAt": "2026-05-07T12:00:00.000Z",
      "clone": {},
      "completedAt": "2026-05-07T12:00:00.000Z",
      "device": {},
      "id": "string",
      "mode": "string",
      "name": "Ava Chen",
      "owner": {},
      "source": "string",
      "startedAt": "2026-05-07T12:00:00.000Z",
      "stoppedAt": "2026-05-07T12:00:00.000Z",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canceledAt` | date |  |
| `clone` | object |  |
| `completedAt` | date |  |
| `device` | object |  |
| `id` | string |  |
| `mode` | string |  |
| `name` | string |  |
| `owner` | object |  |
| `source` | string |  |
| `startedAt` | date |  |
| `stoppedAt` | date |  |
| `user` | object |  |

## Native endpoint

Through the native Bulldog-WP API, this operation is `GET /campaigns/{campaignId}` (base URL `https://api.bulldog-wp.co.il/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

