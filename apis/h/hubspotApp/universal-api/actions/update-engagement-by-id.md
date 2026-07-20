# HubSpot: Update Engagement by ID

Updates an existing engagement record in HubSpot.

```
PUT https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/update-engagement-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/update-engagement-by-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "engagementType": "calls",
  "engagementId": "string",
  "properties": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/update-engagement-by-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "engagementType": "calls",
    "engagementId": "string",
    "properties": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `engagementType` | string | yes | HubSpot activity object type to update. One of: `calls`, `communications`, `emails`, `meetings`, `notes`, `postal_mail`, `tasks`. |
| `engagementId` | string | yes | HubSpot record ID of the engagement to update. |
| `properties` | object | yes | Engagement property values keyed by HubSpot property name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idProperty` | string | no | Optional unique property name to use instead of the internal record ID. |

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

Through the native HubSpot API, this operation is `PATCH crm/v3/objects/:engagementType/:engagementId` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-engagement-by-id.md) for the provider-specific parameters and requirements.

