# Salesforge: List Workspace Sequences

Retrieves workspace sequences from Salesforge.

```
GET https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/list-workspace-sequences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforge `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/list-workspace-sequences?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceID=wks_989gtkhm1ir6z8hdv3gjn" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspaceID": "wks_989gtkhm1ir6z8hdv3gjn"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/list-workspace-sequences?${params}`, {
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
| `workspaceID` | string | yes | Workspace ID to list sequences from. Example: `wks_989gtkhm1ir6z8hdv3gjn`. |
| `statuses` | list<string> | no | Only return sequences in the selected statuses. Accepts multiple values as an array. Example: `draft,active`. |
| `productId` | string | no | Only return sequences for a specific product. Example: `prod_123456`. |
| `sequenceIds` | list<string> | no | Only return the selected sequence IDs. Accepts multiple values as an array. Example: `seq_123456,seq_789012`. |
| `type` | string | no | Only return sequences of the selected type. Example: `legacy`. |

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

Through the native Salesforge API, this operation is `GET /public/v2/workspaces/:workspaceID/sequences` (base URL `https://api.salesforge.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-workspace-sequences.md) for the provider-specific parameters and requirements.

