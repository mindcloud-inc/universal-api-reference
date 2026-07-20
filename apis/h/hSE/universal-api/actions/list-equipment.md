# 4HSE: List Equipment

Retrieves equipment from 4HSE.

```
GET https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-equipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 4HSE `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-equipment?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-equipment?${params}`, {
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
| `filter` | object | no | Search filters. |
| `filter.officeId` | string | no | Filter by office ID. |
| `filter.projectId` | string | no | Filter by project ID. |
| `filter.name` | string | no | Filter by name. |
| `history` | boolean | no | Include historicized equipment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "code": "string",
      "description": "string",
      "equipmentId": "string",
      "model": "string",
      "name": "Ava Chen",
      "officeEquipmentId": "string",
      "officeId": "string",
      "officeName": "Ava Chen",
      "ownedActive": true,
      "parentActive": true,
      "permission": "string",
      "projectId": "string",
      "projectName": "Ava Chen",
      "projectType": "string",
      "serial": "string",
      "vendor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `code` | string |  |
| `description` | string |  |
| `equipmentId` | string |  |
| `model` | string |  |
| `name` | string |  |
| `officeEquipmentId` | string |  |
| `officeId` | string |  |
| `officeName` | string |  |
| `ownedActive` | boolean |  |
| `parentActive` | boolean |  |
| `permission` | string |  |
| `projectId` | string |  |
| `projectName` | string |  |
| `projectType` | string |  |
| `serial` | string |  |
| `vendor` | string |  |

## Native endpoint

Through the native 4HSE API, this operation is `POST /v2/equipment/index` (base URL `https://service.4hse.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-equipment.md) for the provider-specific parameters and requirements.

