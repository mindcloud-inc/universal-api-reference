# HubSpot: Create Quote

Creates a new quote in HubSpot.

```
POST https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-quote" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "properties.hs_title": "string",
  "properties.hs_expiration_date": "2026-05-07T12:00:00.000Z",
  "properties.hs_template_type": "CPQ_QUOTE"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-quote', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "properties.hs_title": "string",
    "properties.hs_expiration_date": "2026-05-07T12:00:00.000Z",
    "properties.hs_template_type": "CPQ_QUOTE"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `properties` | object | no | The quote properties payload. |
| `properties.hs_title` | string | yes | The quote title shown in HubSpot. |
| `properties.hs_expiration_date` | date | yes | When the quote expires. |
| `properties.hs_template_type` | string | yes | Use the HubSpot CPQ template type. This action defaults to CPQ_QUOTE and does not support the legacy quote flow. Default: `CPQ_QUOTE`. |
| `properties.hs_slug` | string | no | Optional quote slug for the hosted quote URL. |
| `associations[]` | array<object> | no | Associations to create with the quote. |
| `associations[].to` | object | no | The association target. |
| `associations[].to.id` | string | no | The associated record ID. |
| `associations[].types[]` | array<object> | no | The association type definitions. |
| `associations[].types[].associationCategory` | string | no | The HubSpot association category. |
| `associations[].types[].associationTypeId` | number | no | The HubSpot association type ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdResourceId": "string",
      "entity": {
        "archived": true,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "properties": {},
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "location": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdResourceId` | string | The created HubSpot quote resource ID. |
| `entity` | object | The created quote payload returned by HubSpot. |
| `entity.archived` | boolean | Whether the quote is archived. |
| `entity.createdAt` | date | When the quote was created. |
| `entity.id` | string | The created quote ID. |
| `entity.properties` | object | The returned quote properties. |
| `entity.updatedAt` | date | When the quote was last updated. |
| `location` | string | The HubSpot API location for the created quote resource. |

## Native endpoint

Through the native HubSpot API, this operation is `POST crm/v3/objects/quotes` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-quote.md) for the provider-specific parameters and requirements.

