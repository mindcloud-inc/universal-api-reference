# HubSpot: Create Project



```
POST https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "properties": {},
  "properties.hs_name": "Ava Chen",
  "properties.hs_pipeline": "string",
  "properties.hs_pipeline_stage": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "properties": {},
    "properties.hs_name": "Ava Chen",
    "properties.hs_pipeline": "string",
    "properties.hs_pipeline_stage": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `properties` | object | yes |  |
| `properties.hs_name` | string | yes |  |
| `properties.hs_pipeline` | string | yes |  |
| `properties.hs_pipeline_stage` | string | yes |  |
| `properties.hs_description` | string | no |  |
| `properties.hs_status` | string | no |  |
| `properties.hs_type` | string | no |  |
| `properties.hs_target_due_date` | date | no |  |
| `properties.hubspot_owner_id` | string | no |  |
| `associations[]` | array<object> | no |  |
| `associations[].to` | object | no |  |
| `associations[].to.id` | string | no |  |
| `associations[].types[]` | array<object> | no |  |
| `associations[].types[].associationCategory` | string | no |  |
| `associations[].types[].associationTypeId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "properties": {},
      "propertiesWithHistory": {},
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
| `archived` | boolean | Whether the project is archived. |
| `archivedAt` | date | When the project was archived. |
| `createdAt` | date | When the project was created. |
| `id` | string | HubSpot project record ID. |
| `properties` | object | Project property values returned by HubSpot. |
| `propertiesWithHistory` | object | Requested project property history. |
| `updatedAt` | date | When the project was last updated. |
| `url` | string | HubSpot project record URL. |

## Native endpoint

Through the native HubSpot API, this operation is `POST crm/objects/2026-03/projects` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

