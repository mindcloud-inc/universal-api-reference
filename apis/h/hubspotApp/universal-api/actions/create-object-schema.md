# HubSpot: Create Object Schema

Creates a new object schema in HubSpot.

```
POST https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-object-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-object-schema" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "labels": {},
  "labels.singular": "string",
  "labels.plural": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-object-schema', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "labels": {},
    "labels.singular": "string",
    "labels.plural": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Internal singular name for the custom object schema. |
| `labels` | object | yes | Singular and plural display labels for the custom object. |
| `labels.singular` | string | yes | Singular display label for the custom object. |
| `labels.plural` | string | yes | Plural display label for the custom object. |
| `description` | string | no | Optional description for the schema. |
| `primaryDisplayProperty` | string | no | Property name used as the primary display label. |
| `searchableProperties[]` | array<string> | no | Property names that should be searchable. |
| `secondaryDisplayProperties[]` | array<string> | no | Property names shown as secondary display fields. |
| `requiredProperties[]` | array<string> | no | Property names HubSpot should require on records. |
| `associatedObjects[]` | array<string> | no | HubSpot standard objects that can associate with this custom object. |
| `properties[]` | array<object> | no | Property definitions to create with the schema. |
| `properties[].name` | string | no | Internal name for a custom property. |
| `properties[].label` | string | no | Display label for a custom property. |
| `properties[].type` | string | no | HubSpot data type for the property. One of: `date`, `datetime`, `enumeration`, `number`, `string`. |
| `properties[].fieldType` | string | no | HubSpot field type for the property. One of: `booleancheckbox`, `checkbox`, `date`, `file`, `number`, `radio`, `select`, `text`, `textarea`. |
| `properties[].groupName` | string | no | Group name for the custom property. |
| `properties[].hasUniqueValue` | boolean | no | Whether HubSpot should enforce unique values for the property. |
| `properties[].isPrimaryDisplayLabel` | boolean | no | Whether this property should be used as the primary display label. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `properties[].options[]` | array<object> | no | Enumeration options for the property. |
| `properties[].options[].label` | string | no | Display label for an enumeration option. |
| `properties[].options[].value` | string | no | Stored value for an enumeration option. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowsSensitiveProperties": true,
      "associatedObjects": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "fullyQualifiedName": "Ava Chen",
      "id": "string",
      "labels": {},
      "metaType": "string",
      "name": "Ava Chen",
      "objectTypeId": "string",
      "primaryDisplayProperty": "string",
      "properties": [
        {}
      ],
      "requiredProperties": [
        "string"
      ],
      "searchableProperties": [
        "string"
      ],
      "secondaryDisplayProperties": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowsSensitiveProperties` | boolean | Whether the schema allows sensitive properties. |
| `associatedObjects` | array<string> | Associated standard objects. |
| `createdAt` | date | When the schema was created. |
| `description` | string | Schema description. |
| `fullyQualifiedName` | string | Fully qualified schema name. |
| `id` | string | HubSpot schema ID. |
| `labels` | object | Singular and plural labels. |
| `metaType` | string | HubSpot schema meta type. |
| `name` | string | Internal schema name. |
| `objectTypeId` | string | HubSpot object type ID for the schema. |
| `primaryDisplayProperty` | string | Primary display property name. |
| `properties` | array<object> | Property definitions on the schema. |
| `requiredProperties` | array<string> | Required property names. |
| `searchableProperties` | array<string> | Searchable property names. |
| `secondaryDisplayProperties` | array<string> | Secondary display property names. |
| `updatedAt` | date | When the schema was last updated. |

## Native endpoint

Through the native HubSpot API, this operation is `POST crm-object-schemas/v3/schemas` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-object-schema.md) for the provider-specific parameters and requirements.

