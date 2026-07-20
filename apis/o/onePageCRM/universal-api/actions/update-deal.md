# OnePageCRM: Update Deal

Updates an existing deal in OnePageCRM.

```
PUT https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/update-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnePageCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/update-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dealId": "Hotel Software"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/update-deal', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dealId": "Hotel Software"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dealId` | list<string> | yes | ID of the deal to update Example: `Hotel Software`. |
| `name` | string | no | Updated deal name Example: `Codex Stage 3 Test Deal`. |
| `status` | list<string> | no | Updated status of the deal One of: `lost`, `pending`, `won`. |
| `contactId` | list<string> | no | ID of the contact the deal belongs to Example: `Joe`. |
| `ownerId` | list<string> | no | ID of the user who owns the deal Example: `apps@mindcloud.co`. |
| `pipelineId` | list<string> | no | ID of the pipeline the deal belongs to Example: `Sales`. |
| `expectedCloseDate` | string | no | Updated expected close date in YYYY-MM-DD format. Example: `2026-04-10`. |
| `amount` | number | no | Updated monetary value of the deal Example: `1250`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text` | string | no | Updated notes related to the deal Example: `Follow-up proposal sent`. |
| `stage` | number | no | Updated progress stage for a pending deal Example: `60`. |
| `salesPipelineId` | list<string> | no | ID of the sales pipeline the deal belongs to Example: `Sales`. |
| `closeDate` | string | no | Updated close date in YYYY-MM-DD format. Example: `2026-03-10`. |
| `date` | string | no | Updated creation date of the deal in YYYY-MM-DD format. Example: `2026-03-10`. |
| `months` | number | no | Updated number of months for a multi-month deal Example: `1`. |
| `cost` | number | no | Updated monetary cost of the deal Example: `0`. |
| `commissionBase` | list<string> | no | Updated base used to calculate the commission One of: `amount`, `margin`. |
| `commissionType` | list<string> | no | Updated type of commission for the deal One of: `absolute`, `none`, `percentage`. |
| `commission` | number | no | Updated commission payable for the deal Example: `0`. |
| `commissionPercentage` | number | no | Updated commission percentage for the deal Example: `0`. |
| `hasDealItems` | boolean | no | Set to true to create or keep deal items |
| `dealItems[].name` | string | no | Name of the deal item Example: `Conference software`. |
| `dealItems[].description` | string | no | Description of the deal item Example: `3 hotels`. |
| `dealItems[].cost` | number | no | Cost of the deal item Example: `0`. |
| `dealItems[].price` | number | no | Price of the deal item Example: `5130`. |
| `dealItems[].qty` | number | no | Quantity of the deal item Example: `1`. |
| `dealItems[].predefinedItemId` | string | no | ID of the predefined item used for deal item creation Example: `69b0275320594670de9e9477`. |
| `dealFields[].dealField.id` | string | no | ID of the deal custom field to update Example: `5aad9b039007ba28c9ebad56`. |
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

Through the native OnePageCRM API, this operation is `PUT /deals/:deal_id` (base URL `https://app.onepagecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-deal.md) for the provider-specific parameters and requirements.

