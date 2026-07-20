# Sertifier: Update Campaign

Updates an existing campaign in Sertifier.

```
PUT https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/update-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sertifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/update-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaign_id": "Campaign ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/update-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaign_id": "Campaign ID"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `badgeId` | string | no |  |
| `campaign_id` | string | yes | Example: `Campaign ID`. |
| `designId` | string | no |  |
| `detailId` | string | no |  |
| `emailFromName` | string | no |  |
| `emailSubject` | string | no |  |
| `emailTemplateId` | string | no |  |
| `title` | string | no |  |
| `emailFromAddress` | string | no | Example: `Leave blank unless SMTP is configured`. |
| `privateCampaign` | boolean | no | Default: `false`. |

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
| `title` | string |  |
| `updateDate` | string |  |

## Native endpoint

Through the native Sertifier API, this operation is `PUT /campaign/:campaign_id` (base URL `https://b2b.sertifier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign.md) for the provider-specific parameters and requirements.

