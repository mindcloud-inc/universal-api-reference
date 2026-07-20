# Teamgate: Create Person

Creates a new person in Teamgate.

```
POST https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/create-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamgate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/create-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teamgate/latest/actions/create-person', {
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
| `name` | string | yes | Person name. |
| `companyId` | string | no | Existing company ID to link to the person. |
| `jobTitle` | string | no | Person job title. |
| `starred` | string | no | Whether the person is starred. Use Teamgate values like yes or no. |
| `source` | string | no | Person source name. |
| `industry` | string | no | Person industry name. |
| `tags` | string | no | Person tags. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerStatusId` | string | no | Customer status ID. |
| `prospectStatusId` | string | no | Prospect status ID. |
| `ownerId` | string | no | Owner user ID. |
| `sourceDescription` | string | no | Person source description. |
| `industryDescription` | string | no | Person industry description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {}
      ],
      "company": {},
      "converted": {},
      "created": {},
      "customerStatus": {},
      "emails": [
        {}
      ],
      "id": 1,
      "industry": {},
      "isDeleted": "string",
      "name": "Ava Chen",
      "owner": {},
      "phones": [
        {}
      ],
      "picture": {},
      "prospectStatus": {},
      "source": {},
      "starred": "string",
      "updated": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> |  |
| `company` | object |  |
| `converted` | object |  |
| `created` | object |  |
| `customerStatus` | object |  |
| `emails` | array<object> |  |
| `id` | number |  |
| `industry` | object |  |
| `isDeleted` | string |  |
| `name` | string |  |
| `owner` | object |  |
| `phones` | array<object> |  |
| `picture` | object |  |
| `prospectStatus` | object |  |
| `source` | object |  |
| `starred` | string |  |
| `updated` | object |  |

## Native endpoint

Through the native Teamgate API, this operation is `POST /people` (base URL `https://api.teamgate.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-person.md) for the provider-specific parameters and requirements.

