# Podio: Get Space

Retrieves an existing space from Podio.

```
GET https://connect.mindcloud.co/v1/universal/podio/latest/actions/get-space
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podio/latest/actions/get-space?connectionId=$CONNECTION_ID&spaceId=123456" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spaceId": "123456"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podio/latest/actions/get-space?${params}`, {
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
| `spaceId` | number | yes | The space ID. Example: `123456`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autoJoin": true,
      "createdBy": {},
      "createdOn": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "isOverdue": true,
      "itemAccountingInfo": {},
      "name": "Ava Chen",
      "org": {},
      "orgId": 1,
      "owner": {},
      "postOnNewApp": true,
      "postOnNewMember": true,
      "premium": true,
      "privacy": "string",
      "push": {},
      "rights": [
        "string"
      ],
      "role": "string",
      "sharefileVaultUrl": "https://example.com",
      "spaceId": 1,
      "subscribed": true,
      "tier": "string",
      "type": "string",
      "url": "https://example.com",
      "urlLabel": "https://example.com",
      "v8EngineUpdated": true,
      "video": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoJoin` | boolean |  |
| `createdBy` | object |  |
| `createdOn` | date |  |
| `description` | string |  |
| `isOverdue` | boolean |  |
| `itemAccountingInfo` | object |  |
| `name` | string |  |
| `org` | object |  |
| `orgId` | number |  |
| `owner` | object |  |
| `postOnNewApp` | boolean |  |
| `postOnNewMember` | boolean |  |
| `premium` | boolean |  |
| `privacy` | string |  |
| `push` | object |  |
| `rights` | array<string> |  |
| `role` | string |  |
| `sharefileVaultUrl` | string |  |
| `spaceId` | number |  |
| `subscribed` | boolean |  |
| `tier` | string |  |
| `type` | string |  |
| `url` | string |  |
| `urlLabel` | string |  |
| `v8EngineUpdated` | boolean |  |
| `video` | string |  |

## Native endpoint

Through the native Podio API, this operation is `GET /space/:space_id` (base URL `https://api.podio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-space.md) for the provider-specific parameters and requirements.

