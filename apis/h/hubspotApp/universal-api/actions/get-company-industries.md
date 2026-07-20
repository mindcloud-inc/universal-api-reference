# HubSpot: Get Company Industries

Retrieves the company industry property from HubSpot.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-company-industries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-company-industries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-company-industries?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataSensitivity` | list<string> | no | The data sensitivity filter to apply. |
| `locale` | string | no | The locale to use when returning property details. |
| `archived` | boolean | no | Whether to include archived property metadata. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calculated": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dataSensitivity": "string",
      "description": "string",
      "displayOrder": 1,
      "externalOptions": true,
      "fieldType": "string",
      "formField": true,
      "groupName": "Ava Chen",
      "hasUniqueValue": true,
      "hidden": true,
      "hubspotDefined": true,
      "label": "string",
      "modificationMetadata": {},
      "name": "Ava Chen",
      "options": [
        {}
      ],
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calculated` | boolean | Whether the property is calculated. |
| `createdAt` | date | When the property definition was created. |
| `dataSensitivity` | string | The property data sensitivity classification. |
| `description` | string | The property description. |
| `displayOrder` | number | The display order of the property. |
| `externalOptions` | boolean | Whether options are externally managed. |
| `fieldType` | string | The field type used in HubSpot. |
| `formField` | boolean | Whether the property can be used on forms. |
| `groupName` | string | The group containing the property. |
| `hasUniqueValue` | boolean | Whether the property enforces unique values. |
| `hidden` | boolean | Whether the property is hidden. |
| `hubspotDefined` | boolean | Whether the property is HubSpot-defined. |
| `label` | string | The display label for the property. |
| `modificationMetadata` | object | Metadata about property mutability. |
| `name` | string | The internal property name. |
| `options` | array<object> | The selectable property options, when present. |
| `type` | string | The storage type for the property. |
| `updatedAt` | date | When the property definition was last updated. |

## Native endpoint

Through the native HubSpot API, this operation is `GET crm/v3/properties/companies/industry` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-industries.md) for the provider-specific parameters and requirements.

