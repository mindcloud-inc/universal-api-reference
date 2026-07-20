# Grist: Get Organization

Retrieves an organization from Grist.

```
GET https://connect.mindcloud.co/v1/universal/grist/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grist/latest/actions/get-organization?connectionId=$CONNECTION_ID&orgId=current" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orgId": "current"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grist/latest/actions/get-organization?${params}`, {
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
| `orgId` | list<number> | yes | Organization ID Default: `current`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access": "string",
      "billingAccount": {
        "externalId": {},
        "externalOptions": {},
        "features": {},
        "id": 1,
        "individual": true,
        "inGoodStanding": true,
        "isManager": true,
        "paid": true,
        "paymentLink": {},
        "product": {
          "features": {
            "baseMaxApiUnitsPerDocumentPerDay": 1,
            "baseMaxAssistantCalls": 1,
            "baseMaxAttachmentsBytesPerDocument": 1,
            "baseMaxDataSizePerDocument": 1,
            "baseMaxRowsPerDocument": 1,
            "gracePeriodDays": 1,
            "maxAttachmentsBytesPerOrg": 1,
            "maxSharesPerDoc": 1,
            "maxSharesPerWorkspace": 1,
            "snapshotWindow": {
              "count": 1,
              "unit": "string"
            },
            "workspaces": true
          },
          "id": 1,
          "name": "Ava Chen"
        },
        "status": {},
        "stripePlanId": {}
      },
      "createdAt": "string",
      "domain": "string",
      "host": {},
      "id": 1,
      "name": "Ava Chen",
      "owner": {
        "createdAt": "string",
        "id": 1,
        "name": "Ava Chen",
        "picture": {},
        "ref": "string",
        "type": "string"
      },
      "updatedAt": "string",
      "userOrgPrefs": {
        "showGristTour": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access` | string |  |
| `billingAccount.externalId` | object |  |
| `billingAccount.externalOptions` | object |  |
| `billingAccount.features` | object |  |
| `billingAccount.id` | number |  |
| `billingAccount.individual` | boolean |  |
| `billingAccount.inGoodStanding` | boolean |  |
| `billingAccount.isManager` | boolean |  |
| `billingAccount.paid` | boolean |  |
| `billingAccount.paymentLink` | object |  |
| `billingAccount.product.features.baseMaxApiUnitsPerDocumentPerDay` | number |  |
| `billingAccount.product.features.baseMaxAssistantCalls` | number |  |
| `billingAccount.product.features.baseMaxAttachmentsBytesPerDocument` | number |  |
| `billingAccount.product.features.baseMaxDataSizePerDocument` | number |  |
| `billingAccount.product.features.baseMaxRowsPerDocument` | number |  |
| `billingAccount.product.features.gracePeriodDays` | number |  |
| `billingAccount.product.features.maxAttachmentsBytesPerOrg` | number |  |
| `billingAccount.product.features.maxSharesPerDoc` | number |  |
| `billingAccount.product.features.maxSharesPerWorkspace` | number |  |
| `billingAccount.product.features.snapshotWindow.count` | number |  |
| `billingAccount.product.features.snapshotWindow.unit` | string |  |
| `billingAccount.product.features.workspaces` | boolean |  |
| `billingAccount.product.id` | number |  |
| `billingAccount.product.name` | string |  |
| `billingAccount.status` | object |  |
| `billingAccount.stripePlanId` | object |  |
| `createdAt` | string |  |
| `domain` | string |  |
| `host` | object |  |
| `id` | number |  |
| `name` | string |  |
| `owner.createdAt` | string |  |
| `owner.id` | number |  |
| `owner.name` | string |  |
| `owner.picture` | object |  |
| `owner.ref` | string |  |
| `owner.type` | string |  |
| `updatedAt` | string |  |
| `userOrgPrefs.showGristTour` | boolean |  |

## Native endpoint

Through the native Grist API, this operation is `GET /orgs/:orgId` (base URL `https://docs.getgrist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

