# DivvyHQ: Get Campaign



```
GET https://connect.mindcloud.co/v1/universal/divvyHQ/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DivvyHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/divvyHQ/latest/actions/get-campaign?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/divvyHQ/latest/actions/get-campaign?${params}`, {
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
| `id` | number | yes | Campaign ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessLevel": "string",
      "account": 1,
      "alwaysInline": true,
      "assignedMembers": [
        {}
      ],
      "attachments": [
        {}
      ],
      "calendars": [
        1
      ],
      "campaignType": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": 1,
      "description": "string",
      "end": "2026-05-07T12:00:00.000Z",
      "hasAttachments": true,
      "id": 1,
      "isArchived": true,
      "name": "Ava Chen",
      "nextActiveTask": {},
      "priority": 1,
      "start": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessLevel` | string |  |
| `account` | number |  |
| `alwaysInline` | boolean |  |
| `assignedMembers` | array<object> |  |
| `attachments` | array<object> |  |
| `calendars` | array<number> |  |
| `campaignType` | number |  |
| `createdAt` | date |  |
| `createdBy` | number |  |
| `description` | string |  |
| `end` | date |  |
| `hasAttachments` | boolean |  |
| `id` | number |  |
| `isArchived` | boolean |  |
| `name` | string |  |
| `nextActiveTask` | object |  |
| `priority` | number |  |
| `start` | date |  |

## Native endpoint

Through the native DivvyHQ API, this operation is `GET /campaigns/:id/` (base URL `https://app.divvyhq.com/api/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

