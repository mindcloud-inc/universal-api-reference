# Oboloo: Create Subcategory

Creates a new subcategory in Oboloo.

```
POST https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/create-subcategory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oboloo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/create-subcategory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "code": "string",
  "subcategory_name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oboloo/latest/actions/create-subcategory', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "code": "string",
    "subcategory_name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `code` | string | yes | Category identifier that this subcategory belongs to. |
| `subcategory_name` | string | yes | Name of the subcategory to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": {
        "code": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "createdBy": 1,
        "id": 1,
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "value": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category.code` | string |  |
| `category.createdAt` | date |  |
| `category.createdBy` | number |  |
| `category.id` | number |  |
| `category.updatedAt` | date |  |
| `category.value` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Oboloo API, this operation is `POST /configuration/addSubCategory` (base URL `https://mindcloudwizard20260330.oboloo.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subcategory.md) for the provider-specific parameters and requirements.

