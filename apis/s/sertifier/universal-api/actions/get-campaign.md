# Sertifier: Get Campaign

Retrieves a campaign from a Sertifier workspace.

```
GET https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/get-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sertifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/get-campaign?connectionId=$CONNECTION_ID&campaign_id=Campaign%20ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaign_id": "Campaign ID"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/get-campaign?${params}`, {
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
| `campaign_id` | string | yes | Example: `Campaign ID`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "badgeId": {},
      "createDate": "string",
      "designId": "string",
      "detailId": "string",
      "emailFromAddress": {},
      "emailFromName": "ava@example.com",
      "emailSubject": "ava@example.com",
      "emailTemplateId": "ava@example.com",
      "id": "string",
      "privateCampaign": true,
      "status": 1,
      "title": "string",
      "updateDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `badgeId` | object |  |
| `createDate` | string |  |
| `designId` | string |  |
| `detailId` | string |  |
| `emailFromAddress` | object |  |
| `emailFromName` | string |  |
| `emailSubject` | string |  |
| `emailTemplateId` | string |  |
| `id` | string |  |
| `privateCampaign` | boolean |  |
| `status` | number |  |
| `title` | string |  |
| `updateDate` | string |  |

## Native endpoint

Through the native Sertifier API, this operation is `GET /campaign/:campaign_id` (base URL `https://b2b.sertifier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign.md) for the provider-specific parameters and requirements.

