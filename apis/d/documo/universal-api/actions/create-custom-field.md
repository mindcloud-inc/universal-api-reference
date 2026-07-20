# Documo: Create Custom Field

Creates a new custom field in Documo.

```
POST https://connect.mindcloud.co/v1/universal/documo/latest/actions/create-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documo/latest/actions/create-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "label": "string",
  "apiName": "Ava Chen",
  "entity": "string",
  "displayUI": true,
  "displayUITable": true,
  "hint": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documo/latest/actions/create-custom-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "label": "string",
    "apiName": "Ava Chen",
    "entity": "string",
    "displayUI": true,
    "displayUITable": true,
    "hint": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `label` | string | yes | String \| Required |
| `apiName` | string | yes | String \| Required |
| `entity` | string | yes | String \| Required \| Possible values: fax, account, user |
| `displayUI` | boolean | yes | Boolean \| Required |
| `displayUITable` | boolean | yes | Boolean \| Required |
| `hint` | string | yes | String \| Required |

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

Through the native Documo API, this operation is `POST /v1/custom-fields` (base URL `https://api.documo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-field.md) for the provider-specific parameters and requirements.

