# HubSpot: List Properties

Retrieves properties from HubSpot.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-properties?connectionId=$CONNECTION_ID&objectType=companies" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "objectType": "companies"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-properties?${params}`, {
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
| `objectType` | string | yes | The object type whose property definitions to list, such as companies or products. Example: `companies`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `properties` | string | no | Comma-separated list of specific property names to include. Accepts multiple values in one string, delimited by `,`. Example: `name,domain`. |
| `dataSensitivity` | list<string> | no | The sensitivity category of properties to return. One of: `highly_sensitive`, `non_sensitive`, `sensitive`. |
| `locale` | string | no | The locale to use for returned property labels and descriptions. Example: `en`. |
| `archived` | boolean | no | Whether to return archived property definitions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "calculated": true,
      "calculationFormula": "string",
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
      "hubspotDefined": true,
      "label": "string",
      "modificationMetadata": {},
      "name": "Ava Chen",
      "options": [
        {}
      ],
      "referencedObjectType": "string",
      "showCurrencySymbol": true,
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
| `archived` | boolean |  |
| `calculated` | boolean |  |
| `calculationFormula` | string |  |
| `createdAt` | date |  |
| `createdUserId` | string |  |
| `dataSensitivity` | string |  |
| `description` | string |  |
| `displayOrder` | number |  |
| `externalOptions` | boolean |  |
| `fieldType` | string |  |
| `formField` | boolean |  |
| `groupName` | string |  |
| `hasUniqueValue` | boolean |  |
| `hidden` | boolean |  |
| `hubspotDefined` | boolean |  |
| `label` | string |  |
| `modificationMetadata` | object |  |
| `name` | string |  |
| `options` | array<object> |  |
| `referencedObjectType` | string |  |
| `showCurrencySymbol` | boolean |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `updatedUserId` | string |  |

## Native endpoint

Through the native HubSpot API, this operation is `GET crm/v3/properties/:objectType` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-properties.md) for the provider-specific parameters and requirements.

