# TalentLMS: Get Course

Retrieves a course from a TalentLMS domain.

```
GET https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/get-course
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentLMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/get-course?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/get-course?${params}`, {
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
| `id` | number | yes | Numeric course ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availability": {},
      "capacity": 1,
      "category": {},
      "code": "string",
      "coverImage": {},
      "creationDate": "string",
      "customFields": [
        {}
      ],
      "description": {},
      "discountedPrice": {},
      "expiresAt": "string",
      "id": 1,
      "introVideo": {},
      "isHiddenFromCatalog": true,
      "isLocked": true,
      "isPrerequisite": true,
      "lastUpdatedOn": "string",
      "level": 1,
      "name": "Ava Chen",
      "price": {},
      "publicKey": "string",
      "rating": {},
      "remainingLicenses": 1,
      "retainAccessAfterCompletion": true,
      "rules": {},
      "startsAt": "string",
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
| `availability` | object |  |
| `capacity` | number |  |
| `category` | object |  |
| `code` | string |  |
| `coverImage` | object |  |
| `creationDate` | string |  |
| `customFields` | array<object> |  |
| `description` | object |  |
| `discountedPrice` | object |  |
| `expiresAt` | string |  |
| `id` | number |  |
| `introVideo` | object |  |
| `isHiddenFromCatalog` | boolean |  |
| `isLocked` | boolean |  |
| `isPrerequisite` | boolean |  |
| `lastUpdatedOn` | string |  |
| `level` | number |  |
| `name` | string |  |
| `price` | object |  |
| `publicKey` | string |  |
| `rating` | object |  |
| `remainingLicenses` | number |  |
| `retainAccessAfterCompletion` | boolean |  |
| `rules` | object |  |
| `startsAt` | string |  |
| `status` | string |  |
| `timeLimit` | number |  |

## Native endpoint

Through the native TalentLMS API, this operation is `GET /courses/:id` (base URL `https://{{credentials.domain}}.talentlms.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-course.md) for the provider-specific parameters and requirements.

