# OnePageCRM: Get Deal

Retrieves a deal from OnePageCRM.

```
GET https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/get-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnePageCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/get-deal?connectionId=$CONNECTION_ID&dealId=Hotel%20Software" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dealId": "Hotel Software"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/get-deal?${params}`, {
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
| `dealId` | list<string> | yes | ID of the deal to retrieve Example: `Hotel Software`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeHistory` | boolean | no | Include deal stage history in the response |

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

Through the native OnePageCRM API, this operation is `GET /deals/:deal_id` (base URL `https://app.onepagecrm.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-deal.md) for the provider-specific parameters and requirements.

