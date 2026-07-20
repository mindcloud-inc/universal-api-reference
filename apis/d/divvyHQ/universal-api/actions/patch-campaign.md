# DivvyHQ: Patch Campaign



```
PUT https://connect.mindcloud.co/v1/universal/divvyHQ/latest/actions/patch-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DivvyHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/divvyHQ/latest/actions/patch-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/divvyHQ/latest/actions/patch-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "accessLevel": "string",
      "account": 1,
      "alwaysInline": true,
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
| `accessLevel` | string | The access level for the campaign. |
| `account` | number | The Divvy account id. |
| `alwaysInline` | boolean | Whether the campaign is always inline. |
| `calendars` | array<number> | The linked calendar ids. |
| `campaignType` | number | The campaign type id. |
| `createdAt` | date | When the campaign was created. |
| `createdBy` | number | The creator member id. |
| `description` | string | The campaign description. |
| `end` | date | The campaign end date. |
| `hasAttachments` | boolean | Whether the campaign has attachments. |
| `id` | number | The campaign id. |
| `isArchived` | boolean | Whether the campaign is archived. |
| `name` | string | The campaign name. |
| `nextActiveTask` | object | The next active production task. |
| `priority` | number | The campaign priority. |
| `start` | date | The campaign start date. |

## Native endpoint

Through the native DivvyHQ API, this operation is `PATCH /campaigns/:id/` (base URL `https://app.divvyhq.com/api/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-campaign.md) for the provider-specific parameters and requirements.

