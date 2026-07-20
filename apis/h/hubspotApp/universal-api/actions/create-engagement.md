# HubSpot: Create Engagement

Creates a new engagement record in HubSpot.

```
POST https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-engagement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-engagement" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "engagementType": "calls",
  "properties": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-engagement', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "engagementType": "calls",
    "properties": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `engagementType` | string | yes | HubSpot activity object type to create. One of: `calls`, `communications`, `emails`, `meetings`, `notes`, `postal_mail`, `tasks`. |
| `properties` | object | yes | Engagement property values keyed by HubSpot property name. |
| `associations[]` | array<object> | no | Associations to create alongside the engagement. |
| `associations[].to.id` | string | no | HubSpot ID of the record to associate. |
| `associations[].types[]` | array<object> | no | Association type definitions for the linked record. |
| `associations[].types[].associationCategory` | string | no | Association category for the linked record. |
| `associations[].types[].associationTypeId` | number | no | Association type identifier for the linked record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "objectWriteTraceId": "string",
      "properties": {},
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the engagement is archived. |
| `createdAt` | date | When the engagement was created. |
| `id` | string | HubSpot engagement record ID. |
| `objectWriteTraceId` | string | HubSpot write trace identifier when returned. |
| `properties` | object | Engagement properties returned by HubSpot. |
| `updatedAt` | date | When the engagement was last updated. |

## Native endpoint

Through the native HubSpot API, this operation is `POST crm/v3/objects/:engagementType` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-engagement.md) for the provider-specific parameters and requirements.

