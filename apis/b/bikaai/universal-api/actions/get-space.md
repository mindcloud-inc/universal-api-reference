# Bika.ai: Get Space

Retrieves a space from Bika.ai.

```
GET https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/get-space
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bika.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/get-space?connectionId=$CONNECTION_ID&spaceId=spcfaZbYtV5hkHSLrDOqY4ve" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spaceId": "spcfaZbYtV5hkHSLrDOqY4ve"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bikaai/latest/actions/get-space?${params}`, {
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
| `spaceId` | string | yes | Bika.ai space ID. Example: `spcfaZbYtV5hkHSLrDOqY4ve`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "createBy": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "logo": {},
        "memberCount": 1,
        "name": "Ava Chen",
        "owner": "string",
        "settings": {},
        "subscription": {
          "plan": "string",
          "planName": "Ava Chen"
        }
      },
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data.createBy` | string |  |
| `data.createdAt` | date |  |
| `data.id` | string |  |
| `data.logo` | object |  |
| `data.memberCount` | number |  |
| `data.name` | string |  |
| `data.owner` | string |  |
| `data.settings` | object |  |
| `data.subscription` | object |  |
| `data.subscription.plan` | string |  |
| `data.subscription.planName` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Bika.ai API, this operation is `GET /spaces/:spaceId` (base URL `https://bika.ai/api/openapi/bika/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-space.md) for the provider-specific parameters and requirements.

