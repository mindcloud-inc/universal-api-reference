# Salesforge: Create Sequence

Creates a sequence in Salesforge.

```
POST https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/create-sequence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/create-sequence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceID": "wks_989gtkhm1ir6z8hdv3gjn",
  "name": "Q2 Expansion Sequence",
  "productId": "prod_123456",
  "language": "american_english",
  "timezone": "America/New_York"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/create-sequence', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceID": "wks_989gtkhm1ir6z8hdv3gjn",
    "name": "Q2 Expansion Sequence",
    "productId": "prod_123456",
    "language": "american_english",
    "timezone": "America/New_York"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceID` | string | yes | Workspace ID from the Salesforge workspace URL or List Workspaces action. Example: `wks_989gtkhm1ir6z8hdv3gjn`. |
| `name` | string | yes | Name of the sequence to create. Example: `Q2 Expansion Sequence`. |
| `productId` | string | yes | Product ID to associate with the sequence. Example: `prod_123456`. |
| `language` | string | yes | Language used by the sequence. Example: `american_english`. |
| `timezone` | string | yes | IANA timezone for the sequence. Example: `America/New_York`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bouncedCount": 1,
      "bouncedPercent": 1,
      "clickedCount": 1,
      "clickedPercent": 1,
      "clickTrackingEnabled": true,
      "companyOutreachLimitCount": 1,
      "companyOutreachLimitEnabled": true,
      "completedCount": 1,
      "completedPercent": 1,
      "contactedCount": 1,
      "id": "string",
      "leadCount": 1,
      "localizedOptOutEnabled": true,
      "name": "Ava Chen",
      "openedCount": 1,
      "openedPercent": 1,
      "openTrackingEnabled": true,
      "productId": "string",
      "repliedCount": 1,
      "repliedPercent": 1,
      "repliedPositiveCount": 1,
      "repliedPositivePercent": 1,
      "sequentialCompanySendingEnabled": true,
      "status": "string",
      "steps": [
        {
          "distributionStrategy": "string",
          "id": "string",
          "name": "Ava Chen",
          "order": 1,
          "variants": [
            {
              "contactInformationSource": "string",
              "distributionWeight": 1,
              "dynamicLanguageEnabled": true,
              "emailContent": "ava@example.com",
              "emailSubject": "ava@example.com",
              "id": "string",
              "isGenerated": true,
              "label": "string",
              "order": 1,
              "overdriveEnabled": true,
              "status": "string",
              "tonality": "string"
            }
          ],
          "waitDays": 1
        }
      ],
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bouncedCount` | number |  |
| `bouncedPercent` | number |  |
| `clickedCount` | number |  |
| `clickedPercent` | number |  |
| `clickTrackingEnabled` | boolean |  |
| `companyOutreachLimitCount` | number |  |
| `companyOutreachLimitEnabled` | boolean |  |
| `completedCount` | number |  |
| `completedPercent` | number |  |
| `contactedCount` | number |  |
| `id` | string |  |
| `leadCount` | number |  |
| `localizedOptOutEnabled` | boolean |  |
| `name` | string |  |
| `openedCount` | number |  |
| `openedPercent` | number |  |
| `openTrackingEnabled` | boolean |  |
| `productId` | string |  |
| `repliedCount` | number |  |
| `repliedPercent` | number |  |
| `repliedPositiveCount` | number |  |
| `repliedPositivePercent` | number |  |
| `sequentialCompanySendingEnabled` | boolean |  |
| `status` | string |  |
| `steps[].distributionStrategy` | string |  |
| `steps[].id` | string |  |
| `steps[].name` | string |  |
| `steps[].order` | number |  |
| `steps[].variants[].contactInformationSource` | string |  |
| `steps[].variants[].distributionWeight` | number |  |
| `steps[].variants[].dynamicLanguageEnabled` | boolean |  |
| `steps[].variants[].emailContent` | string |  |
| `steps[].variants[].emailSubject` | string |  |
| `steps[].variants[].id` | string |  |
| `steps[].variants[].isGenerated` | boolean |  |
| `steps[].variants[].label` | string |  |
| `steps[].variants[].order` | number |  |
| `steps[].variants[].overdriveEnabled` | boolean |  |
| `steps[].variants[].status` | string |  |
| `steps[].variants[].tonality` | string |  |
| `steps[].waitDays` | number |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Salesforge API, this operation is `POST /public/v2/workspaces/:workspaceID/sequences` (base URL `https://api.salesforge.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sequence.md) for the provider-specific parameters and requirements.

