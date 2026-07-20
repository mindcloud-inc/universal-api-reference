# Swipe One: Create Contact Property



```
POST https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/create-contact-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swipe One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/create-contact-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "label": "string",
  "fieldType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/create-contact-property', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "label": "string",
    "fieldType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | yes | Unique identifier of the workspace where the contact property will be created. |
| `label` | string | yes | The human-readable label for the contact property. |
| `name` | string | no | The unique name of the contact property. |
| `fieldType` | string | yes | The field type for the contact property. |
| `numberFormat` | string | no | Number format when field type is number. |
| `currency` | string | no | Currency code when number format is currency. |
| `dateFormat` | string | no | Date format when field type is date. |
| `includeTime` | boolean | no | Whether to include time when field type is date. |
| `addressFields` | object | no | Address field configuration when field type is address. |
| `options` | list<object> | no | Selectable options when field type is select or multiselect. |
| `optionsName` | string | no | Optional group name for selectable options. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "dataType": "string",
      "fieldType": "string",
      "Id": "string",
      "isArchived": true,
      "isEnabled": true,
      "label": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `createdAt` | date |  |
| `createdBy` | object |  |
| `dataType` | string |  |
| `fieldType` | string |  |
| `Id` | string |  |
| `isArchived` | boolean |  |
| `isEnabled` | boolean |  |
| `label` | string |  |
| `name` | string |  |
| `updatedAt` | date |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Swipe One API, this operation is `POST /workspaces/:workspaceId/contact-properties` (base URL `https://api.swipeone.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact-property.md) for the provider-specific parameters and requirements.

