# HubSpot: Create Listings (v2026-03)

Creates a listing in HubSpot.

```
PUT https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-listings-v202603
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-listings-v202603" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "properties": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-listings-v202603', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "properties": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `properties` | object | yes | Object of company properties to update, e.g. {"arr":"250000"}. |
| `associations[]` | array<object> | no | ### Associations Use this field to associate the new Listing with existing HubSpot records, such as contacts, companies, deals, or other supported CRM objects. Provide an array of association objects using the following structure: ```json [ { "to": { "id": "123456789" }, "types": [ { "associationCategory": "HUBSPOT_DEFINED", "associationTypeId": 882 } ] } ] ``` Each association must include: * `to.id`: The HubSpot record ID of the existing record you want to associate with the new Listing. * `types`: An array describing the relationship between the Listing and the associated record. * `associationCategory`: Use `HUBSPOT_DEFINED` for standard HubSpot associations or `USER_DEFINED` for custom association labels. * `associationTypeId`: The numeric ID of the association type or label. You may include multiple objects in the array to associate the Listing with more than one record. Example with multiple associations: ```json [ { "to": { "id": "123456789" }, "types": [ { "associationCategory": "HUBSPOT_DEFINED", "associationTypeId": 882 } ] }, { "to": { "id": "987654321" }, "types": [ { "associationCategory": "HUBSPOT_DEFINED", "associationTypeId": 884 } ] } ] ``` The correct `associationTypeId` depends on the target object type and association label configured in the connected HubSpot account. |

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
| `archived` | boolean | Whether the company is archived. |
| `createdAt` | date | When the company was created. |
| `id` | string | The company record ID. |
| `properties` | object | The returned company properties. |
| `updatedAt` | date | When the company was last updated. |
| `url` | string | The HubSpot company URL. |

## Native endpoint

Through the native HubSpot API, this operation is `POST crm/objects/2026-03/listings` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-listings-v202603.md) for the provider-specific parameters and requirements.

