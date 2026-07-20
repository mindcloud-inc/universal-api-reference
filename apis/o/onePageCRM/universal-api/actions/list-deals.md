# OnePageCRM: List Deals

Retrieves deals from OnePageCRM.

```
GET https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-deals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnePageCRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-deals?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-deals?${params}`, {
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
| `name` | string | no | Search deals by name Example: `Hotel Software`. |
| `search` | string | no | Search deals by deal name, contact name, or company name Example: `Acme Inc.`. |
| `status` | list<string> | no | Return deals of a particular status One of: `closed`, `lost`, `pending`, `won`. |
| `pipelineId` | list<string> | no | Return deals from the specified pipeline Example: `Sales`. |
| `ownerId` | list<string> | no | Return deals owned by a specific user Example: `apps@mindcloud.co`. |
| `companyId` | list<string> | no | Return deals for a specific company Example: `Acme Inc.`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `salesPipelineId` | list<string> | no | Return deals referencing the specified sales pipeline Example: `Sales`. |
| `contactId` | list<string> | no | Return deals for a specific contact Example: `Joe`. |
| `tag` | string | no | Filter deals by tag Example: `VIP`. |
| `filterId` | string | no | Apply a saved filter to the deal listing Example: `5ae9cc2a9007ba5b856c7bb8`. |
| `stage` | number | no | Return pending deals with the specified deal stage Example: `60`. |
| `dateFilter` | list<string> | no | Choose which date field to use with date-range filtering One of: `close_date`, `created_at`, `date`, `expected_close_date`, `modified_at`, `updated_at`. |
| `since` | date | no | Start of the date range filter Example: `2026-03-01`. |
| `until` | date | no | End of the date range filter Example: `2026-03-31`. |
| `modifiedSince` | date | no | Return only resources that were modified since the specified time Example: `2026-03-01`. |
| `unmodifiedSince` | date | no | Return only resources that were unmodified since the specified time Example: `2026-03-01`. |
| `includeHistory` | boolean | no | Include deal stage history in the response |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "author": "string",
      "closeDate": "2026-05-07T12:00:00.000Z",
      "commission": 1,
      "commissionBase": "string",
      "commissionPercentage": 1,
      "commissionType": "string",
      "contactId": "string",
      "contactInfo": {
        "company": "string",
        "contactName": "Ava Chen",
        "contactOwnerId": "string",
        "photoUrl": "https://example.com"
      },
      "cost": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "date": "2026-05-07T12:00:00.000Z",
      "expectedCloseDate": "2026-05-07T12:00:00.000Z",
      "hasDealItems": true,
      "hasRelatedNotes": true,
      "id": "string",
      "lastStage": {},
      "lastTimelineUpdate": "2026-05-07T12:00:00.000Z",
      "margin": 1,
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "months": 1,
      "name": "Ava Chen",
      "owner": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "ownerId": "string",
      "pipelineId": "string",
      "salesPipelineId": "string",
      "stage": 1,
      "status": "string",
      "text": "string",
      "totalAmount": 1,
      "totalCost": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `author` | string |  |
| `closeDate` | date |  |
| `commission` | number |  |
| `commissionBase` | string |  |
| `commissionPercentage` | number |  |
| `commissionType` | string |  |
| `contactId` | string |  |
| `contactInfo.company` | string |  |
| `contactInfo.contactName` | string |  |
| `contactInfo.contactOwnerId` | string |  |
| `contactInfo.photoUrl` | string |  |
| `cost` | number |  |
| `createdAt` | date |  |
| `date` | date |  |
| `expectedCloseDate` | date |  |
| `hasDealItems` | boolean |  |
| `hasRelatedNotes` | boolean |  |
| `id` | string |  |
| `lastStage` | object |  |
| `lastTimelineUpdate` | date |  |
| `margin` | number |  |
| `modifiedAt` | date |  |
| `months` | number |  |
| `name` | string |  |
| `owner.email` | string |  |
| `owner.id` | string |  |
| `owner.name` | string |  |
| `ownerId` | string |  |
| `pipelineId` | string |  |
| `salesPipelineId` | string |  |
| `stage` | number |  |
| `status` | string |  |
| `text` | string |  |
| `totalAmount` | number |  |
| `totalCost` | number |  |

## Native endpoint

Through the native OnePageCRM API, this operation is `GET /deals` (base URL `https://app.onepagecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-deals.md) for the provider-specific parameters and requirements.

