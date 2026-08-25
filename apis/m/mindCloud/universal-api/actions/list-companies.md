# MindCloud: List Companies



```
GET https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MindCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/list-companies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/list-companies?${params}`, {
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
| `name` | string | no | Example: `ACME Corp.`. |
| `isDeleted` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "createdOn": "string",
          "description": "string",
          "id": "string",
          "isDeleted": true,
          "isPersonal": true,
          "name": "Ava Chen",
          "settings": {
            "allowSameDomainDiscovery": true,
            "apps": [
              {
                "appId": "string",
                "description": "string",
                "id": "string"
              }
            ],
            "companyContacts": [
              {
                "email": "ava@example.com",
                "id": "string",
                "jobTitle": "string",
                "name": "Ava Chen",
                "type": "string"
              }
            ],
            "companyDomains": [
              "string"
            ],
            "companyWebsite": "string",
            "credentialExchangeSigningSecret": "string",
            "customSenderAddress": {
              "label": "string",
              "value": 1
            },
            "description": "string",
            "embeddedAppId": "string",
            "enableEmbedded": true,
            "enableTurnkeyIntegrations": true,
            "exchangeRoute": "string",
            "lastCredentialExchangeTestOn": "string",
            "overviewQuestions": [
              "string"
            ],
            "provisioningRoute": "string",
            "routeWorkflowsThroughNATGateway": true,
            "signingSignatureEnabled": true,
            "solution": "string",
            "turnkeyIntegrationsEndUserId": "string",
            "useCustomSenderAddress": true,
            "workflowStages": true,
            "xSignatureEnabled": true
          },
          "timezone": "string",
          "updatedOn": "string"
        }
      ],
      "meta": {
        "pagination": {
          "hasNextPage": true,
          "hasPreviousPage": true,
          "totalCount": 1
        }
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].createdOn` | string |  |
| `data[].description` | string |  |
| `data[].id` | string |  |
| `data[].isDeleted` | boolean |  |
| `data[].isPersonal` | boolean |  |
| `data[].name` | string |  |
| `data[].settings.allowSameDomainDiscovery` | boolean |  |
| `data[].settings.apps[].appId` | string |  |
| `data[].settings.apps[].description` | string |  |
| `data[].settings.apps[].id` | string |  |
| `data[].settings.companyContacts[].email` | string |  |
| `data[].settings.companyContacts[].id` | string |  |
| `data[].settings.companyContacts[].jobTitle` | string |  |
| `data[].settings.companyContacts[].name` | string |  |
| `data[].settings.companyContacts[].type` | string |  |
| `data[].settings.companyDomains[]` | string |  |
| `data[].settings.companyWebsite` | string |  |
| `data[].settings.credentialExchangeSigningSecret` | string |  |
| `data[].settings.customSenderAddress.label` | string |  |
| `data[].settings.customSenderAddress.value` | number |  |
| `data[].settings.description` | string |  |
| `data[].settings.embeddedAppId` | string |  |
| `data[].settings.enableEmbedded` | boolean |  |
| `data[].settings.enableTurnkeyIntegrations` | boolean |  |
| `data[].settings.exchangeRoute` | string |  |
| `data[].settings.lastCredentialExchangeTestOn` | string |  |
| `data[].settings.overviewQuestions[]` | string |  |
| `data[].settings.provisioningRoute` | string |  |
| `data[].settings.routeWorkflowsThroughNATGateway` | boolean |  |
| `data[].settings.signingSignatureEnabled` | boolean |  |
| `data[].settings.solution` | string |  |
| `data[].settings.turnkeyIntegrationsEndUserId` | string |  |
| `data[].settings.useCustomSenderAddress` | boolean |  |
| `data[].settings.workflowStages` | boolean |  |
| `data[].settings.xSignatureEnabled` | boolean |  |
| `data[].timezone` | string |  |
| `data[].updatedOn` | string |  |
| `meta.pagination.hasNextPage` | boolean |  |
| `meta.pagination.hasPreviousPage` | boolean |  |
| `meta.pagination.totalCount` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native MindCloud API, this operation is `GET v1/companies` (base URL `https://embedded.mindcloud.co/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

