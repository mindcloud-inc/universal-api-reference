# HubSpot: Create Property

Creates a new property in HubSpot.

```
POST https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "objectType": "string",
  "groupName": "Ava Chen",
  "name": "Ava Chen",
  "label": "string",
  "type": "bool",
  "fieldType": "booleancheckbox"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-property', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "objectType": "string",
    "groupName": "Ava Chen",
    "name": "Ava Chen",
    "label": "string",
    "type": "bool",
    "fieldType": "booleancheckbox"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `objectType` | string | yes | The HubSpot object type that will own the property, such as contacts, companies, deals, tickets, products, or a custom object type. |
| `groupName` | string | yes | The existing HubSpot property group that will contain the property. |
| `name` | string | yes | The internal property name, for example favorite_food. |
| `label` | string | yes | The display label shown in HubSpot. |
| `type` | list | yes | The HubSpot data type for the property. One of: `bool`, `date`, `datetime`, `enumeration`, `number`, `string`. |
| `fieldType` | list | yes | How the property should be rendered in HubSpot. One of: `booleancheckbox`, `calculation_equation`, `checkbox`, `date`, `file`, `html`, `number`, `phonenumber`, `radio`, `select`, `text`, `textarea`. |
| `description` | string | no | Optional description for the property. |
| `hasUniqueValue` | boolean | no | Whether HubSpot should enforce unique values for the property. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `options[]` | array<object> | no | Enumeration options for the property. |
| `options[].label` | string | no | Display label for an enumeration option. |
| `options[].value` | string | no | Stored value for an enumeration option. |
| `calculationFormula` | string | no | Formula used when creating a calculation property. |
| `externalOptions` | boolean | no | Whether the property options should be populated dynamically from HubSpot instead of a static option list. |
| `referencedObjectType` | list | no | The HubSpot object type that provides external option values. Use OWNER for HubSpot user-picker fields. One of: `OWNER`. |
| `formField` | boolean | no | Whether the property can be used on HubSpot forms. |
| `displayOrder` | number | no | Display order within the property group. HubSpot places -1 after positive values. |
| `hidden` | boolean | no | Whether the property should be hidden in HubSpot. |
| `dataSensitivity` | list | no | Sensitivity classification for the property. One of: `highly_sensitive`, `non_sensitive`, `sensitive`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "calculated": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdUserId": "string",
      "dataSensitivity": "string",
      "description": "string",
      "displayOrder": 1,
      "externalOptions": true,
      "fieldType": "string",
      "formField": true,
      "groupName": "Ava Chen",
      "hasUniqueValue": true,
      "hidden": true,
      "label": "string",
      "modificationMetadata": {},
      "name": "Ava Chen",
      "options": [
        {}
      ],
      "referencedObjectType": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedUserId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the property is archived. |
| `calculated` | boolean | Whether the property is a calculated property. |
| `createdAt` | date | When the property definition was created. |
| `createdUserId` | string | The user ID that created the property. |
| `dataSensitivity` | string | The HubSpot data sensitivity classification for the property. |
| `description` | string | The property description. |
| `displayOrder` | number | The HubSpot display order for the property. |
| `externalOptions` | boolean | Whether the property uses externally managed options. |
| `fieldType` | string | How the property is rendered in HubSpot. |
| `formField` | boolean | Whether the property can be used on forms. |
| `groupName` | string | The property group that owns the property. |
| `hasUniqueValue` | boolean | Whether HubSpot enforces unique values for the property. |
| `hidden` | boolean | Whether the property is hidden in HubSpot. |
| `label` | string | The HubSpot display label for the property. |
| `modificationMetadata` | object | HubSpot metadata describing whether the property can be archived or edited. |
| `name` | string | The internal property name. |
| `options` | array<object> | Enumeration options for the property. |
| `referencedObjectType` | string | The HubSpot object type used for external option-backed properties. |
| `type` | string | The HubSpot property type. |
| `updatedAt` | date | When the property definition was last updated. |
| `updatedUserId` | string | The user ID that last updated the property. |

## Native endpoint

Through the native HubSpot API, this operation is `POST crm/v3/properties/:objectType` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-property.md) for the provider-specific parameters and requirements.

