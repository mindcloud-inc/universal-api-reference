# Umbler Talk: Get Channel

Retrieves a channel from Umbler Talk.

```
GET https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/get-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbler Talk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/get-channel?connectionId=$CONNECTION_ID&id=string&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/get-channel?${params}`, {
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
| `id` | string | yes | The channel ID. |
| `organizationId` | string | yes | The organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_t": "string",
      "channelType": "string",
      "createdAtUTC": "2026-05-07T12:00:00.000Z",
      "displayName": "Ava Chen",
      "groupIds": [
        "string"
      ],
      "id": "string",
      "organization": {},
      "phoneNumber": "string",
      "pictureUrl": "https://example.com",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_t` | string |  |
| `channelType` | string |  |
| `createdAtUTC` | date |  |
| `displayName` | string |  |
| `groupIds` | array<string> |  |
| `id` | string |  |
| `organization` | object |  |
| `phoneNumber` | string |  |
| `pictureUrl` | string |  |
| `state` | string |  |

## Native endpoint

Through the native Umbler Talk API, this operation is `GET /v1/channels/[:id]/` (base URL `https://app-utalk.umbler.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel.md) for the provider-specific parameters and requirements.

