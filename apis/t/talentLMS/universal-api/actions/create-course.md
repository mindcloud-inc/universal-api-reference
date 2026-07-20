# TalentLMS: Create Course

Creates a new course in TalentLMS.

```
POST https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/create-course
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentLMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/create-course" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/create-course', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Course name. |
| `code` | string | no | Course code. |
| `description` | string | no | Course description. |
| `categoryId` | number | no | Course category ID. |
| `price` | number | no | Course price. |
| `capacity` | number | no | Course capacity. |
| `level` | number | no | Course level. |
| `timeLimit` | number | no | Course time limit. |
| `startDatetime` | string | no | Course start datetime. |
| `expirationDatetime` | string | no | Course expiration datetime. |
| `isActive` | boolean | no | Whether the course is active. |
| `customFields` | object | no | Custom fields object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capacity": 1,
      "category": {},
      "code": "string",
      "creationDate": "string",
      "description": {},
      "discountedPrice": {},
      "id": 1,
      "isHiddenFromCatalog": true,
      "isLocked": true,
      "lastUpdatedOn": "string",
      "level": 1,
      "name": "Ava Chen",
      "price": {},
      "status": "string",
      "timeLimit": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capacity` | number |  |
| `category` | object |  |
| `code` | string |  |
| `creationDate` | string |  |
| `description` | object |  |
| `discountedPrice` | object |  |
| `id` | number |  |
| `isHiddenFromCatalog` | boolean |  |
| `isLocked` | boolean |  |
| `lastUpdatedOn` | string |  |
| `level` | number |  |
| `name` | string |  |
| `price` | object |  |
| `status` | string |  |
| `timeLimit` | number |  |

## Native endpoint

Through the native TalentLMS API, this operation is `POST /courses` (base URL `https://{{credentials.domain}}.talentlms.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-course.md) for the provider-specific parameters and requirements.

