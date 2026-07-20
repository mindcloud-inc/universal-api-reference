# Documo: Archive Custom Field

Archives an existing custom field in Documo.

```
PUT https://connect.mindcloud.co/v1/universal/documo/latest/actions/archive-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/documo/latest/actions/archive-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customFieldId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documo/latest/actions/archive-custom-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customFieldId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customFieldId` | string | yes | String \| Required \| Custom Field UUID |
| `isArchived` | boolean | no | Boolean |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "apiName": "Ava Chen",
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "displayUI": true,
      "displayUITable": true,
      "entity": "string",
      "hint": "string",
      "isArchived": true,
      "label": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `apiName` | string |  |
| `archivedAt` | date |  |
| `createdAt` | date |  |
| `displayUI` | boolean |  |
| `displayUITable` | boolean |  |
| `entity` | string |  |
| `hint` | string |  |
| `isArchived` | boolean |  |
| `label` | string |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Documo API, this operation is `PATCH /v1/custom-fields/:customFieldId` (base URL `https://api.documo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/archive-custom-field.md) for the provider-specific parameters and requirements.

