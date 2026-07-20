# OnePageCRM: Create Deal

Creates a new deal in OnePageCRM.

```
POST https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/create-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnePageCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/create-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "Joe",
  "ownerId": "apps@mindcloud.co",
  "name": "Codex Stage 3 Test Deal"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/create-deal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "Joe",
    "ownerId": "apps@mindcloud.co",
    "name": "Codex Stage 3 Test Deal"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | list<string> | yes | ID of the contact the deal belongs to Example: `Joe`. |
| `ownerId` | list<string> | yes | ID of the user who owns the deal Example: `apps@mindcloud.co`. |
| `name` | string | yes | Name of the deal Example: `Codex Stage 3 Test Deal`. |
| `pipelineId` | list<string> | no | ID of the pipeline the deal belongs to Example: `Sales`. |
| `status` | list<string> | no | Status of the deal One of: `lost`, `pending`, `won`. |
| `expectedCloseDate` | string | no | Date the deal is expected to close in YYYY-MM-DD format. Example: `2026-04-10`. |
| `amount` | number | no | Monetary value of the deal Example: `1250`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `salesPipelineId` | list<string> | no | ID of the sales pipeline the deal belongs to Example: `Sales`. |
| `stage` | number | no | Progress stage for a pending deal Example: `60`. |
| `closeDate` | string | no | Date the deal actually closed in YYYY-MM-DD format. Example: `2026-03-10`. |
| `date` | string | no | Creation date of the deal in YYYY-MM-DD format. Example: `2026-03-10`. |
| `months` | number | no | Number of months for a multi-month deal Example: `1`. |
| `cost` | number | no | Monetary cost of the deal Example: `0`. |
| `commissionBase` | list<string> | no | Base used to calculate the commission One of: `amount`, `margin`. |
| `commissionType` | list<string> | no | Type of commission for the deal One of: `absolute`, `none`, `percentage`. |
| `commission` | number | no | Commission payable for the deal Example: `0`. |
| `commissionPercentage` | number | no | Commission percentage for the deal Example: `0`. |
| `text` | string | no | Extra notes related to the deal Example: `Follow-up proposal sent`. |
| `hasDealItems` | boolean | no | Set to true to create or keep deal items |
| `dealItems[].name` | string | no | Name of the deal item Example: `Conference software`. |
| `dealItems[].description` | string | no | Description of the deal item Example: `3 hotels`. |
| `dealItems[].cost` | number | no | Cost of the deal item Example: `0`. |
| `dealItems[].price` | number | no | Price of the deal item Example: `5130`. |
| `dealItems[].qty` | number | no | Quantity of the deal item Example: `1`. |
| `dealItems[].predefinedItemId` | string | no | ID of the predefined item used for deal item creation Example: `69b0275320594670de9e9477`. |
| `dealFields[].dealField.id` | string | no | ID of the deal custom field to set Example: `5aad9b039007ba28c9ebad56`. |
| `dealFields[].value` | string | no | Value for the deal custom field Example: `Large`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "author": "string",
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

Through the native OnePageCRM API, this operation is `POST /deals` (base URL `https://app.onepagecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deal.md) for the provider-specific parameters and requirements.

