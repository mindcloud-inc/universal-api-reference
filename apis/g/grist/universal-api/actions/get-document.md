# Grist: Get Document

Retrieves a document from Grist.

```
GET https://connect.mindcloud.co/v1/universal/grist/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grist/latest/actions/get-document?connectionId=$CONNECTION_ID&docId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grist/latest/actions/get-document?${params}`, {
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
| `docId` | string | yes | Document ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access": "string",
      "aliases": [
        {
          "createdAt": "string",
          "docId": "string",
          "orgId": 1,
          "urlId": "https://example.com"
        }
      ],
      "createdAt": "string",
      "id": "string",
      "isPinned": true,
      "name": "Ava Chen",
      "trunkId": {},
      "type": {},
      "updatedAt": "string",
      "urlId": "https://example.com",
      "workspace": {
        "access": "string",
        "createdAt": "string",
        "id": 1,
        "isSupportWorkspace": true,
        "name": "Ava Chen",
        "org": {
          "access": "string",
          "billingAccount": {
            "externalId": {},
            "externalOptions": {},
            "features": {},
            "id": 1,
            "individual": true,
            "inGoodStanding": true,
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
          "updatedAt": "string"
        },
        "owner": {
          "createdAt": "string",
          "id": 1,
          "name": "Ava Chen",
          "picture": {},
          "ref": "string",
          "type": "string"
        },
        "updatedAt": "string"
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
| `aliases[].createdAt` | string |  |
| `aliases[].docId` | string |  |
| `aliases[].orgId` | number |  |
| `aliases[].urlId` | string |  |
| `createdAt` | string |  |
| `id` | string |  |
| `isPinned` | boolean |  |
| `name` | string |  |
| `trunkId` | object |  |
| `type` | object |  |
| `updatedAt` | string |  |
| `urlId` | string |  |
| `workspace.access` | string |  |
| `workspace.createdAt` | string |  |
| `workspace.id` | number |  |
| `workspace.isSupportWorkspace` | boolean |  |
| `workspace.name` | string |  |
| `workspace.org.access` | string |  |
| `workspace.org.billingAccount.externalId` | object |  |
| `workspace.org.billingAccount.externalOptions` | object |  |
| `workspace.org.billingAccount.features` | object |  |
| `workspace.org.billingAccount.id` | number |  |
| `workspace.org.billingAccount.individual` | boolean |  |
| `workspace.org.billingAccount.inGoodStanding` | boolean |  |
| `workspace.org.billingAccount.paymentLink` | object |  |
| `workspace.org.billingAccount.product.features.baseMaxApiUnitsPerDocumentPerDay` | number |  |
| `workspace.org.billingAccount.product.features.baseMaxAssistantCalls` | number |  |
| `workspace.org.billingAccount.product.features.baseMaxAttachmentsBytesPerDocument` | number |  |
| `workspace.org.billingAccount.product.features.baseMaxDataSizePerDocument` | number |  |
| `workspace.org.billingAccount.product.features.baseMaxRowsPerDocument` | number |  |
| `workspace.org.billingAccount.product.features.gracePeriodDays` | number |  |
| `workspace.org.billingAccount.product.features.maxAttachmentsBytesPerOrg` | number |  |
| `workspace.org.billingAccount.product.features.maxSharesPerDoc` | number |  |
| `workspace.org.billingAccount.product.features.maxSharesPerWorkspace` | number |  |
| `workspace.org.billingAccount.product.features.snapshotWindow.count` | number |  |
| `workspace.org.billingAccount.product.features.snapshotWindow.unit` | string |  |
| `workspace.org.billingAccount.product.features.workspaces` | boolean |  |
| `workspace.org.billingAccount.product.id` | number |  |
| `workspace.org.billingAccount.product.name` | string |  |
| `workspace.org.billingAccount.status` | object |  |
| `workspace.org.billingAccount.stripePlanId` | object |  |
| `workspace.org.createdAt` | string |  |
| `workspace.org.domain` | string |  |
| `workspace.org.host` | object |  |
| `workspace.org.id` | number |  |
| `workspace.org.name` | string |  |
| `workspace.org.owner.createdAt` | string |  |
| `workspace.org.owner.id` | number |  |
| `workspace.org.owner.name` | string |  |
| `workspace.org.owner.picture` | object |  |
| `workspace.org.owner.ref` | string |  |
| `workspace.org.owner.type` | string |  |
| `workspace.org.updatedAt` | string |  |
| `workspace.owner.createdAt` | string |  |
| `workspace.owner.id` | number |  |
| `workspace.owner.name` | string |  |
| `workspace.owner.picture` | object |  |
| `workspace.owner.ref` | string |  |
| `workspace.owner.type` | string |  |
| `workspace.updatedAt` | string |  |

## Native endpoint

Through the native Grist API, this operation is `GET /docs/:docId` (base URL `https://docs.getgrist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

