# CATS: Get Job

Retrieves details for a job in CATS.

```
GET https://connect.mindcloud.co/v1/universal/cATS/latest/actions/get-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cATS/latest/actions/get-job?connectionId=$CONNECTION_ID&id=16789175" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "16789175"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cATS/latest/actions/get-job?${params}`, {
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
| `id` | number | yes | The ID of the job to return. Example: `16789175`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryName": "Ava Chen",
      "companyId": 1,
      "contactId": {},
      "countryCode": {},
      "dateCreated": "string",
      "dateModified": "string",
      "departmentId": {},
      "description": {},
      "duration": {},
      "Embedded": {
        "applications": [
          {
            "description": "string",
            "Embedded": {
              "fields": [
                {
                  "applicationId": 1,
                  "comment": "string",
                  "id": 1,
                  "isRequired": true,
                  "linkedCustomFieldId": {},
                  "Links": {
                    "self": {
                      "href": "https://example.com"
                    }
                  },
                  "minItems": {},
                  "position": 1,
                  "savesToField": "string",
                  "size": {},
                  "title": "string",
                  "type": "string"
                }
              ]
            },
            "header": "string",
            "id": 1,
            "Links": {
              "fields": {
                "href": "https://example.com"
              },
              "self": {
                "href": "https://example.com"
              }
            }
          }
        ],
        "company": {
          "address": {
            "city": {},
            "postalCode": {},
            "state": {},
            "street": {}
          },
          "billingContactId": {},
          "countryCode": {},
          "dateCreated": "string",
          "dateModified": "string",
          "enteredById": 1,
          "id": 1,
          "isHot": true,
          "keyTechnologies": {},
          "Links": {
            "self": {
              "href": "https://example.com"
            }
          },
          "name": "Ava Chen",
          "notes": "string",
          "ownerId": 1,
          "phones": {
            "fax": {},
            "primary": {},
            "secondary": {}
          },
          "statusId": 1,
          "website": {}
        },
        "status": {
          "id": 1,
          "Links": {
            "self": {
              "href": "https://example.com"
            }
          },
          "mapping": "string",
          "title": "string",
          "workflowId": 1
        }
      },
      "externalId": {},
      "id": 1,
      "isHot": true,
      "isPublished": true,
      "Links": {
        "applications": {
          "href": "https://example.com"
        },
        "attachments": {
          "href": "https://example.com"
        },
        "company": {
          "href": "https://example.com"
        },
        "customFields": {
          "href": "https://example.com"
        },
        "pipelines": {
          "href": "https://example.com"
        },
        "self": {
          "href": "https://example.com"
        },
        "status": {
          "href": "https://example.com"
        },
        "tags": {
          "href": "https://example.com"
        }
      },
      "location": {
        "city": "string",
        "postalCode": "string",
        "state": "string"
      },
      "maxRate": {},
      "notes": {},
      "openings": 1,
      "ownerId": 1,
      "pipelineWorkflowId": {},
      "portalHidden": true,
      "recruiterId": {},
      "remoteType": {},
      "salary": {},
      "sourcerId": {},
      "startDate": {},
      "statusId": 1,
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryName` | string |  |
| `companyId` | number |  |
| `contactId` | object |  |
| `countryCode` | object |  |
| `dateCreated` | string |  |
| `dateModified` | string |  |
| `departmentId` | object |  |
| `description` | object |  |
| `duration` | object |  |
| `Embedded.applications[].description` | string |  |
| `Embedded.applications[].Embedded.fields[].applicationId` | number |  |
| `Embedded.applications[].Embedded.fields[].comment` | string |  |
| `Embedded.applications[].Embedded.fields[].id` | number |  |
| `Embedded.applications[].Embedded.fields[].isRequired` | boolean |  |
| `Embedded.applications[].Embedded.fields[].linkedCustomFieldId` | object |  |
| `Embedded.applications[].Embedded.fields[].Links.self.href` | string |  |
| `Embedded.applications[].Embedded.fields[].minItems` | object |  |
| `Embedded.applications[].Embedded.fields[].position` | number |  |
| `Embedded.applications[].Embedded.fields[].savesToField` | string |  |
| `Embedded.applications[].Embedded.fields[].size` | object |  |
| `Embedded.applications[].Embedded.fields[].title` | string |  |
| `Embedded.applications[].Embedded.fields[].type` | string |  |
| `Embedded.applications[].header` | string |  |
| `Embedded.applications[].id` | number |  |
| `Embedded.applications[].Links.fields.href` | string |  |
| `Embedded.applications[].Links.self.href` | string |  |
| `Embedded.company.address.city` | object |  |
| `Embedded.company.address.postalCode` | object |  |
| `Embedded.company.address.state` | object |  |
| `Embedded.company.address.street` | object |  |
| `Embedded.company.billingContactId` | object |  |
| `Embedded.company.countryCode` | object |  |
| `Embedded.company.dateCreated` | string |  |
| `Embedded.company.dateModified` | string |  |
| `Embedded.company.enteredById` | number |  |
| `Embedded.company.id` | number |  |
| `Embedded.company.isHot` | boolean |  |
| `Embedded.company.keyTechnologies` | object |  |
| `Embedded.company.Links.self.href` | string |  |
| `Embedded.company.name` | string |  |
| `Embedded.company.notes` | string |  |
| `Embedded.company.ownerId` | number |  |
| `Embedded.company.phones.fax` | object |  |
| `Embedded.company.phones.primary` | object |  |
| `Embedded.company.phones.secondary` | object |  |
| `Embedded.company.statusId` | number |  |
| `Embedded.company.website` | object |  |
| `Embedded.status.id` | number |  |
| `Embedded.status.Links.self.href` | string |  |
| `Embedded.status.mapping` | string |  |
| `Embedded.status.title` | string |  |
| `Embedded.status.workflowId` | number |  |
| `externalId` | object |  |
| `id` | number |  |
| `isHot` | boolean |  |
| `isPublished` | boolean |  |
| `Links.applications.href` | string |  |
| `Links.attachments.href` | string |  |
| `Links.company.href` | string |  |
| `Links.customFields.href` | string |  |
| `Links.pipelines.href` | string |  |
| `Links.self.href` | string |  |
| `Links.status.href` | string |  |
| `Links.tags.href` | string |  |
| `location.city` | string |  |
| `location.postalCode` | string |  |
| `location.state` | string |  |
| `maxRate` | object |  |
| `notes` | object |  |
| `openings` | number |  |
| `ownerId` | number |  |
| `pipelineWorkflowId` | object |  |
| `portalHidden` | boolean |  |
| `recruiterId` | object |  |
| `remoteType` | object |  |
| `salary` | object |  |
| `sourcerId` | object |  |
| `startDate` | object |  |
| `statusId` | number |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native CATS API, this operation is `GET /jobs/:id` (base URL `https://api.catsone.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job.md) for the provider-specific parameters and requirements.

