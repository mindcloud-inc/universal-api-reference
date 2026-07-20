# HubSpot: Create Contact

Creates a new contact in HubSpot.

```
POST https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "properties": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-contact', {
  method: 'POST',
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
| `associations[].to` | object | no |  |
| `associations[].to.id` | string | no | Id of the object to associate |
| `associations[].types[].associationCategory` | list<string> | no | This represents if the association you're creating is default created by HupSpot, or it is a custom association the user defined. |
| `properties` | object | yes |  |
| `associations[]` | array<object> | no |  |
| `associations[].types[]` | array | no |  |
| `associations[].types[].associationTypeId` | string | no | Check for types at: https://developers.hubspot.com/docs/api-reference/crm-associations-v4/guide#association-type-id-values |
| `properties.firstname` | string | no |  |
| `properties.lastname` | string | no |  |
| `properties.email` | string | no |  |
| `properties.mobilephone` | string | no |  |
| `properties.phone` | string | no |  |
| `properties.jobtitle` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "string",
      "id": "string",
      "properties": {
        "createdate": "string",
        "email": "ava@example.com",
        "firstname": "Ava",
        "hsObjectId": "string",
        "lastmodifieddate": "string",
        "lastname": "Chen"
      },
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `createdAt` | string |  |
| `id` | string |  |
| `properties.createdate` | string |  |
| `properties.email` | string |  |
| `properties.firstname` | string |  |
| `properties.hsObjectId` | string |  |
| `properties.lastmodifieddate` | string |  |
| `properties.lastname` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |

## Native endpoint

Through the native HubSpot API, this operation is `POST crm/v3/objects/contacts` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

