# Apollo: Bulk Create Accounts

Creates multiple new accounts in Apollo.

```
POST https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/bulk-create-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apollo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/bulk-create-accounts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accounts[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/bulk-create-accounts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accounts[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accounts[]` | array<object> | yes | Array of account attribute objects (maximum 100 accounts per request) |
| `accounts[].name` | string | no | Account name |
| `accounts[].domain` | string | no | Company domain (e.g., 'example.com') |
| `accounts[].ownerId` | string | no | Account owner user ID (BSON::ObjectId format). Defaults to current user if not provided |
| `accounts[].phone` | string | no | Company phone number |
| `accounts[].phoneStatusCd` | string | no | Phone validation status |
| `accounts[].rawAddress` | string | no | Company address |
| `accounts[].linkedinUrl` | string | no | LinkedIn company page URL |
| `accounts[].facebookUrl` | string | no | Facebook page URL |
| `accounts[].twitterUrl` | string | no | Twitter profile URL |
| `accounts[].salesforceId` | string | no | Salesforce account ID for CRM integration |
| `accounts[].hubspotId` | string | no | HubSpot company ID for CRM integration |
| `accounts[].mergedCrmIds[]` | array<string> | no | Additional CRM IDs for deduplication |
| `accounts[].organizationId` | string | no | Apollo organization ID |
| `accounts[].parentAccountId` | string | no | Parent account ID for account hierarchy (BSON::ObjectId format) |
| `accounts[].accountStageId` | string | no | Account stage/pipeline stage ID (BSON::ObjectId format) |
| `accounts[].typedCustomFields` | object | no | Custom field values as key-value pairs where key is the field_id and value is the field_value |
| `accounts[].appendLabelNames[]` | array<string> | no | Label names to apply to the account |
| `runDedupe` | boolean | no | Enable aggressive deduplication by domain, organization_id, and name. When false (default), only matches by CRM IDs. When true, also matches by domain, organization_id, and name. Existing accounts are returned without modification in both modes |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAccounts": [
        {
          "accountStageId": "string",
          "city": "string",
          "country": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "creatorId": "string",
          "crmOwnerId": {},
          "crmRecordUrl": {},
          "domain": "string",
          "existenceLevel": "string",
          "facebookUrl": {},
          "hubspotId": {},
          "id": "string",
          "intentStrength": {},
          "linkedinUrl": {},
          "modality": "string",
          "name": "Ava Chen",
          "organizationHeadcountSixMonthGrowth": {},
          "organizationHeadcountTwelveMonthGrowth": {},
          "organizationHeadcountTwentyFourMonthGrowth": {},
          "organizationId": "string",
          "originalSource": "string",
          "ownerId": "string",
          "parentAccountId": {},
          "phone": {},
          "phoneStatus": "string",
          "postalCode": "string",
          "rawAddress": "string",
          "salesforceId": {},
          "showIntent": true,
          "source": "string",
          "sourceDisplayName": "Ava Chen",
          "state": "string",
          "streetAddress": "string",
          "suggestedFromRuleEngineConfigId": {},
          "teamId": "string",
          "twitterUrl": {}
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAccounts[].accountStageId` | string |  |
| `createdAccounts[].city` | string |  |
| `createdAccounts[].country` | string |  |
| `createdAccounts[].createdAt` | date |  |
| `createdAccounts[].creatorId` | string |  |
| `createdAccounts[].crmOwnerId` | object |  |
| `createdAccounts[].crmRecordUrl` | object |  |
| `createdAccounts[].domain` | string |  |
| `createdAccounts[].existenceLevel` | string |  |
| `createdAccounts[].facebookUrl` | object |  |
| `createdAccounts[].hubspotId` | object |  |
| `createdAccounts[].id` | string |  |
| `createdAccounts[].intentStrength` | object |  |
| `createdAccounts[].linkedinUrl` | object |  |
| `createdAccounts[].modality` | string |  |
| `createdAccounts[].name` | string |  |
| `createdAccounts[].organizationHeadcountSixMonthGrowth` | object |  |
| `createdAccounts[].organizationHeadcountTwelveMonthGrowth` | object |  |
| `createdAccounts[].organizationHeadcountTwentyFourMonthGrowth` | object |  |
| `createdAccounts[].organizationId` | string |  |
| `createdAccounts[].originalSource` | string |  |
| `createdAccounts[].ownerId` | string |  |
| `createdAccounts[].parentAccountId` | object |  |
| `createdAccounts[].phone` | object |  |
| `createdAccounts[].phoneStatus` | string |  |
| `createdAccounts[].postalCode` | string |  |
| `createdAccounts[].rawAddress` | string |  |
| `createdAccounts[].salesforceId` | object |  |
| `createdAccounts[].showIntent` | boolean |  |
| `createdAccounts[].source` | string |  |
| `createdAccounts[].sourceDisplayName` | string |  |
| `createdAccounts[].state` | string |  |
| `createdAccounts[].streetAddress` | string |  |
| `createdAccounts[].suggestedFromRuleEngineConfigId` | object |  |
| `createdAccounts[].teamId` | string |  |
| `createdAccounts[].twitterUrl` | object |  |

## Native endpoint

Through the native Apollo API, this operation is `POST v1/accounts/bulk_create` (base URL `https://app.apollo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-create-accounts.md) for the provider-specific parameters and requirements.

