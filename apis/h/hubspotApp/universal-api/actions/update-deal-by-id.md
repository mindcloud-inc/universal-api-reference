# HubSpot: Update Deal by ID

Updates an existing deal in HubSpot.

```
PUT https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/update-deal-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/update-deal-by-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dealId": "string",
  "properties": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/update-deal-by-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dealId": "string",
    "properties": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dealId` | string | yes | HubSpot deal record ID to update. |
| `properties` | object | yes | Object of deal properties to update, for example {"dealstage":"appointmentscheduled"}. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idProperty` | string | no | Unique property used to identify the deal instead of the internal record ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "properties": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the deal is archived. |
| `createdAt` | date | When the deal was created. |
| `id` | string | The HubSpot deal record ID. |
| `properties` | object | The returned HubSpot deal properties. |
| `updatedAt` | date | When the deal was last updated. |
| `url` | string | The HubSpot deal URL. |

## Native endpoint

Through the native HubSpot API, this operation is `PATCH crm/v3/objects/deals/:dealId` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-deal-by-id.md) for the provider-specific parameters and requirements.

