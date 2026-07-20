# CompanyHub: List Records

Retrieves records from a specific CompanyHub table.

```
GET https://connect.mindcloud.co/v1/universal/companyHub/latest/actions/list-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CompanyHub `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companyHub/latest/actions/list-records?connectionId=$CONNECTION_ID&limit=25&offset=0&tableName=Contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "tableName": "Contact"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companyHub/latest/actions/list-records?${params}`, {
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
| `tableName` | string | yes | Exact CompanyHub API table name, for example Contact, Company, Deal, or a custom table name. Example: `Contact`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": "string",
      "city": "string",
      "company": {
        "id": 1,
        "name": "Ava Chen"
      },
      "country": "string",
      "createdBy": {
        "id": 1,
        "name": "Ava Chen"
      },
      "createdOn": "2026-05-07T12:00:00.000Z",
      "deletedBy": {
        "id": 1,
        "name": "Ava Chen"
      },
      "description": "string",
      "designation": "string",
      "email": "ava@example.com",
      "facebook": "string",
      "firstName": "Ava",
      "googlePlus": "string",
      "hasOptedOutOfEmails": true,
      "hotness": "string",
      "id": 1,
      "lastName": "Chen",
      "linkedIn": "https://example.com",
      "modifiedBy": {
        "id": 1,
        "name": "Ava Chen"
      },
      "modifiedOn": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "nextFollowUpDate": "2026-05-07T12:00:00.000Z",
      "noFollowups": true,
      "owner": {
        "id": 1,
        "name": "Ava Chen"
      },
      "phone": "string",
      "postalCode": "string",
      "skype": "string",
      "source": "string",
      "state": "string",
      "street": "string",
      "tag": "string",
      "twitter": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string |  |
| `city` | string |  |
| `company.id` | number |  |
| `company.name` | string |  |
| `country` | string |  |
| `createdBy.id` | number |  |
| `createdBy.name` | string |  |
| `createdOn` | date |  |
| `deletedBy.id` | number |  |
| `deletedBy.name` | string |  |
| `description` | string |  |
| `designation` | string |  |
| `email` | string |  |
| `facebook` | string |  |
| `firstName` | string |  |
| `googlePlus` | string |  |
| `hasOptedOutOfEmails` | boolean |  |
| `hotness` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `linkedIn` | string |  |
| `modifiedBy.id` | number |  |
| `modifiedBy.name` | string |  |
| `modifiedOn` | date |  |
| `name` | string |  |
| `nextFollowUpDate` | date |  |
| `noFollowups` | boolean |  |
| `owner.id` | number |  |
| `owner.name` | string |  |
| `phone` | string |  |
| `postalCode` | string |  |
| `skype` | string |  |
| `source` | string |  |
| `state` | string |  |
| `street` | string |  |
| `tag` | string |  |
| `twitter` | string |  |

## Native endpoint

Through the native CompanyHub API, this operation is `GET /tables/:tableName` (base URL `https://api.companyhub.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-records.md) for the provider-specific parameters and requirements.

