# SOS Inventory: List Builds



```
GET https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-builds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SOS Inventory `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-builds?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/list-builds?${params}`, {
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
| `query` | string | no | Match build number, ID, comment, location, or output item name. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `archived` | list<string> | no | One of: `no`, `yes`. |
| `from` | date | no | Example: `2026-01-01T00:00:00`. |
| `to` | date | no | Example: `2026-01-01T00:00:00`. |
| `location` | list<string> | no |  |
| `createdSince` | date | no | Example: `2026-01-01T00:00:00`. |
| `updatedSince` | date | no | Example: `2026-01-01T00:00:00`. |
| `summary` | string | no | Any supplied value returns summary fields only. Leave empty for complete records. Example: `yes`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "comment": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "hasSignature": true,
      "id": 1,
      "inputs": [
        {
          "class": {
            "id": 1,
            "name": "Ava Chen"
          },
          "description": "string",
          "id": 1,
          "item": {
            "id": 1,
            "name": "Ava Chen"
          },
          "lineNumber": 1,
          "lot": {
            "id": 1,
            "name": "Ava Chen"
          },
          "quantity": 1,
          "volume": 1,
          "volumeunit": "string",
          "waste": true,
          "weight": 1,
          "weightunit": "string"
        }
      ],
      "location": {
        "id": 1,
        "name": "Ava Chen"
      },
      "number": "string",
      "outputs": [
        {
          "class": {
            "id": 1,
            "name": "Ava Chen"
          },
          "description": "string",
          "id": 1,
          "item": {
            "id": 1,
            "name": "Ava Chen"
          },
          "lineNumber": 1,
          "lot": {
            "id": 1,
            "name": "Ava Chen"
          },
          "lotExpiration": "2026-05-07T12:00:00.000Z",
          "notes": "string",
          "quantity": 1,
          "volume": 1,
          "volumeunit": "string",
          "waste": true,
          "weight": 1,
          "weightunit": "string"
        }
      ],
      "starred": 1,
      "summaryOnly": true,
      "syncToken": 1,
      "total": 1,
      "workcenter": {
        "id": 1,
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `comment` | string |  |
| `date` | date |  |
| `hasSignature` | boolean |  |
| `id` | number |  |
| `inputs` | array<object> |  |
| `inputs[].class.id` | number |  |
| `inputs[].class.name` | string |  |
| `inputs[].description` | string |  |
| `inputs[].id` | number |  |
| `inputs[].item.id` | number |  |
| `inputs[].item.name` | string |  |
| `inputs[].lineNumber` | number |  |
| `inputs[].lot.id` | number |  |
| `inputs[].lot.name` | string |  |
| `inputs[].quantity` | number |  |
| `inputs[].volume` | number |  |
| `inputs[].volumeunit` | string |  |
| `inputs[].waste` | boolean |  |
| `inputs[].weight` | number |  |
| `inputs[].weightunit` | string |  |
| `location.id` | number |  |
| `location.name` | string |  |
| `number` | string |  |
| `outputs` | array<object> |  |
| `outputs[].class.id` | number |  |
| `outputs[].class.name` | string |  |
| `outputs[].description` | string |  |
| `outputs[].id` | number |  |
| `outputs[].item.id` | number |  |
| `outputs[].item.name` | string |  |
| `outputs[].lineNumber` | number |  |
| `outputs[].lot.id` | number |  |
| `outputs[].lot.name` | string |  |
| `outputs[].lotExpiration` | date |  |
| `outputs[].notes` | string |  |
| `outputs[].quantity` | number |  |
| `outputs[].volume` | number |  |
| `outputs[].volumeunit` | string |  |
| `outputs[].waste` | boolean |  |
| `outputs[].weight` | number |  |
| `outputs[].weightunit` | string |  |
| `starred` | number |  |
| `summaryOnly` | boolean |  |
| `syncToken` | number |  |
| `total` | number |  |
| `workcenter.id` | number |  |
| `workcenter.name` | string |  |

## Native endpoint

Through the native SOS Inventory API, this operation is `GET /api/v2/build` (base URL `https://api.sosinventory.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-builds.md) for the provider-specific parameters and requirements.

