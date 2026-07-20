# Productive.io: List Companies

Retrieves companies from your Productive.io account.

```
GET https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productive.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-companies?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "archivedAt": "string",
        "avatarUrl": "https://example.com",
        "billingName": "Ava Chen",
        "companyCode": "string",
        "contact": {
          "addresses": [
            {}
          ],
          "phones": [
            {}
          ],
          "websites": [
            {}
          ]
        },
        "createdAt": "string",
        "customFields": "string",
        "defaultCurrency": "string",
        "defaultDocumentTypeId": "string",
        "defaultSubsidiaryId": "string",
        "defaultTaxRateId": "string",
        "domain": "string",
        "dueDays": 1,
        "externalId": "string",
        "externalSync": true,
        "lastActivityAt": "string",
        "name": "Ava Chen",
        "originalAvatarUrl": "https://example.com",
        "parentCompanyId": "string",
        "projectlessBudgets": true,
        "sampleData": true,
        "tagList": [
          "string"
        ],
        "vat": "string"
      },
      "id": "string",
      "relationships": {
        "customFieldAttachments": {
          "meta": {
            "included": true
          }
        },
        "customFieldPeople": {
          "meta": {
            "included": true
          }
        },
        "defaultSubsidiary": {
          "meta": {
            "included": true
          }
        },
        "defaultTaxRate": {
          "meta": {
            "included": true
          }
        },
        "einvoiceIdentity": {
          "meta": {
            "included": true
          }
        },
        "integrationExporterConfiguration": {
          "meta": {
            "included": true
          }
        },
        "organization": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "parentCompany": {
          "data": "string"
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.archivedAt` | string |  |
| `attributes.avatarUrl` | string |  |
| `attributes.billingName` | string |  |
| `attributes.companyCode` | string |  |
| `attributes.contact.addresses` | array<object> |  |
| `attributes.contact.phones` | array<object> |  |
| `attributes.contact.websites` | array<object> |  |
| `attributes.createdAt` | string |  |
| `attributes.customFields` | string |  |
| `attributes.defaultCurrency` | string |  |
| `attributes.defaultDocumentTypeId` | string |  |
| `attributes.defaultSubsidiaryId` | string |  |
| `attributes.defaultTaxRateId` | string |  |
| `attributes.domain` | string |  |
| `attributes.dueDays` | number |  |
| `attributes.externalId` | string |  |
| `attributes.externalSync` | boolean |  |
| `attributes.lastActivityAt` | string |  |
| `attributes.name` | string |  |
| `attributes.originalAvatarUrl` | string |  |
| `attributes.parentCompanyId` | string |  |
| `attributes.projectlessBudgets` | boolean |  |
| `attributes.sampleData` | boolean |  |
| `attributes.tagList` | array<string> |  |
| `attributes.vat` | string |  |
| `id` | string |  |
| `relationships.customFieldAttachments.meta.included` | boolean |  |
| `relationships.customFieldPeople.meta.included` | boolean |  |
| `relationships.defaultSubsidiary.meta.included` | boolean |  |
| `relationships.defaultTaxRate.meta.included` | boolean |  |
| `relationships.einvoiceIdentity.meta.included` | boolean |  |
| `relationships.integrationExporterConfiguration.meta.included` | boolean |  |
| `relationships.organization.data.id` | string |  |
| `relationships.organization.data.type` | string |  |
| `relationships.parentCompany.data` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Productive.io API, this operation is `GET /companies` (base URL `https://api.productive.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-companies.md) for the provider-specific parameters and requirements.

