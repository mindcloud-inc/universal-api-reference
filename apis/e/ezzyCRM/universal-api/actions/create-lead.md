# EzzyCRM: Create Lead



```
POST https://connect.mindcloud.co/v1/universal/ezzyCRM/latest/actions/create-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EzzyCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ezzyCRM/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactModel.firstName": "Ava",
  "contactModel.lastName": "Chen",
  "organizationModel.organizationName": "Ava Chen",
  "userId": 1,
  "dealTitle": "string",
  "dealCurrencyId": 1,
  "pipelineId": 1,
  "stageCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ezzyCRM/latest/actions/create-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactModel.firstName": "Ava",
    "contactModel.lastName": "Chen",
    "organizationModel.organizationName": "Ava Chen",
    "userId": 1,
    "dealTitle": "string",
    "dealCurrencyId": 1,
    "pipelineId": 1,
    "stageCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactModel` | object | no |  |
| `contactModel.firstName` | string | yes |  |
| `contactModel.lastName` | string | yes |  |
| `contactModel.email` | string | no |  |
| `contactModel.title` | string | no |  |
| `contactModel.phoneType` | string | no |  |
| `contactModel.phone` | string | no |  |
| `contactModel.remark` | string | no |  |
| `organizationModel` | object | no |  |
| `organizationModel.organizationName` | string | yes |  |
| `organizationModel.address1` | string | no |  |
| `organizationModel.address2` | string | no |  |
| `organizationModel.city` | string | no |  |
| `organizationModel.zipCode` | string | no |  |
| `organizationModel.stateName` | string | no |  |
| `organizationModel.countryName` | string | no |  |
| `organizationModel.industryName` | string | no |  |
| `userId` | number | yes |  |
| `dealTitle` | string | yes |  |
| `dealValue` | string | no |  |
| `dealCurrencyId` | number | yes |  |
| `noteModel[]` | array<string> | no |  |
| `pipelineId` | number | yes |  |
| `stageCode` | string | yes |  |
| `expectedCloseDate` | string | no | Expected close date in MM/DD/YYYY format. Example: `04/30/2026`. |
| `customField1` | string | no |  |
| `customField2` | string | no |  |
| `customField3` | string | no |  |
| `customField4` | string | no |  |
| `customField5` | string | no |  |
| `customField6` | string | no |  |
| `customField7` | string | no |  |
| `customField8` | string | no |  |
| `customField9` | string | no |  |
| `customField10` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "dealId": 1,
      "dealTitle": "string",
      "dealValue": "string",
      "pipelineId": 1,
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `dealId` | number |  |
| `dealTitle` | string |  |
| `dealValue` | string |  |
| `pipelineId` | number |  |
| `userId` | number |  |

## Native endpoint

Through the native EzzyCRM API, this operation is `POST /api/savelead` (base URL `https://ezzycrm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead.md) for the provider-specific parameters and requirements.

