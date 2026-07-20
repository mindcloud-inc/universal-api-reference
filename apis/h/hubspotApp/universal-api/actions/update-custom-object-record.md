# HubSpot: Update Custom Object Record

Updates a custom object record in HubSpot.

```
PUT https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/update-custom-object-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/update-custom-object-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "objectType": "2-56303805",
  "objectId": "45903597154",
  "properties": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/update-custom-object-record', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "objectType": "2-56303805",
    "objectId": "45903597154",
    "properties": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `objectType` | string | yes | Custom object type ID or fully qualified name, for example `2-56303805`. Example: `2-56303805`. |
| `objectId` | string | yes | HubSpot custom object record ID to update. Example: `45903597154`. |
| `properties` | object | yes | Object of custom object properties to update, for example `{"source_app":"cirra"}`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idProperty` | string | no | Unique property used to identify the record instead of the internal record ID. Example: `tracking_number`. |

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
| `archived` | boolean | Whether the record is archived. |
| `createdAt` | date | The timestamp when the record was created. |
| `id` | string | The unique ID of the updated record. |
| `properties` | object | Key-value pairs representing the updated record properties. |
| `updatedAt` | date | The timestamp when the record was last updated. |
| `url` | string | Direct URL for this record in HubSpot when available. |

## Native endpoint

Through the native HubSpot API, this operation is `PATCH crm/v3/objects/:objectType/:objectId` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-custom-object-record.md) for the provider-specific parameters and requirements.

