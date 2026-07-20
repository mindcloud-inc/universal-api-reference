# Moosend: Get Campaign Details

Retrieves campaign details from Moosend.

```
GET https://connect.mindcloud.co/v1/universal/moosend/latest/actions/get-campaign-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moosend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moosend/latest/actions/get-campaign-details?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moosend/latest/actions/get-campaign-details?${params}`, {
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
| `campaignId` | string | yes | The ID of the campaign that contains the details you are requesting. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abCampaignData": "string",
      "confirmationTo": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "deliveredOn": "2026-05-07T12:00:00.000Z",
      "formatType": 1,
      "htmlContent": "string",
      "id": "string",
      "isTransactional": true,
      "mailingLists": [
        {}
      ],
      "name": "Ava Chen",
      "plainContent": "string",
      "replyToEmail": {},
      "scheduledFor": "string",
      "sender": {},
      "status": 1,
      "subject": "string",
      "timezone": "string",
      "updatedOn": "2026-05-07T12:00:00.000Z",
      "webLocation": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abCampaignData` | string |  |
| `confirmationTo` | string |  |
| `createdOn` | date |  |
| `deliveredOn` | date |  |
| `formatType` | number |  |
| `htmlContent` | string |  |
| `id` | string |  |
| `isTransactional` | boolean |  |
| `mailingLists` | array<object> |  |
| `name` | string |  |
| `plainContent` | string |  |
| `replyToEmail` | object |  |
| `scheduledFor` | string |  |
| `sender` | object |  |
| `status` | number |  |
| `subject` | string |  |
| `timezone` | string |  |
| `updatedOn` | date |  |
| `webLocation` | string |  |

## Native endpoint

Through the native Moosend API, this operation is `GET /campaigns/{{CampaignID}}/view.json` (base URL `https://api.moosend.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-details.md) for the provider-specific parameters and requirements.

