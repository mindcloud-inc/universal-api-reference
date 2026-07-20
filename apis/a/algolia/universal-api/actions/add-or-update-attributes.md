# Algolia: Add or Update Attributes

Adds or updates record attributes in Algolia.

```
PUT https://connect.mindcloud.co/v1/universal/algolia/latest/actions/add-or-update-attributes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/add-or-update-attributes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "indexName": "Ava Chen",
  "objectID": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/algolia/latest/actions/add-or-update-attributes', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "indexName": "Ava Chen",
    "objectID": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `indexName` | string | yes | The name of the Algolia index. |
| `objectID` | string | yes | Unique identifier for the record. |
| `name` | string | no | Record name or title. |
| `category` | string | no | Category value for faceting or filtering. |
| `brand` | string | no | Brand value for the record. |
| `color` | string | no | Color value for the record. |
| `price` | number | no | Numeric price for the record. |
| `isPublished` | boolean | no | Whether the record is published. |
| `tags[]` | array<string> | no | Tag values for the record. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createIfNotExists` | boolean | no | Whether to create the record if it does not exist. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "objectID": "string",
      "taskID": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `objectID` | string |  |
| `taskID` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Algolia API, this operation is `POST /1/indexes/:indexName/:objectID/partial` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-or-update-attributes.md) for the provider-specific parameters and requirements.

