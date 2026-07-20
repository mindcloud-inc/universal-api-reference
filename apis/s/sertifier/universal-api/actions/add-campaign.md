# Sertifier: Add Campaign

Creates a new campaign in Sertifier.

```
POST https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/add-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sertifier `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/add-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "Operational Issuance Test Campaign",
  "detailId": "Existing detail id",
  "designId": "Existing certificate design id",
  "emailTemplateId": "Existing email template id",
  "emailFromName": "MindCloud Test Sender",
  "emailSubject": "MindCloud Operational Issuance Test",
  "emailFromAddress": "apps@mindcloud.co"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sertifier/latest/actions/add-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "Operational Issuance Test Campaign",
    "detailId": "Existing detail id",
    "designId": "Existing certificate design id",
    "emailTemplateId": "Existing email template id",
    "emailFromName": "MindCloud Test Sender",
    "emailSubject": "MindCloud Operational Issuance Test",
    "emailFromAddress": "apps@mindcloud.co"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Example: `Operational Issuance Test Campaign`. |
| `detailId` | string | yes | Example: `Existing detail id`. |
| `designId` | string | yes | Example: `Existing certificate design id`. |
| `emailTemplateId` | string | yes | Example: `Existing email template id`. |
| `emailFromName` | string | yes | Example: `MindCloud Test Sender`. |
| `emailSubject` | string | yes | Example: `MindCloud Operational Issuance Test`. |
| `emailFromAddress` | string | yes | Example: `apps@mindcloud.co`. |
| `badgeId` | string | no | Example: `Existing badge design id (optional)`. |
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

Through the native Sertifier API, this operation is `POST /campaign` (base URL `https://b2b.sertifier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-campaign.md) for the provider-specific parameters and requirements.

