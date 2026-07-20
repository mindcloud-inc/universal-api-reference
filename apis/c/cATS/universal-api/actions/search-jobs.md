# CATS: Search Jobs

Finds jobs in CATS by search query.

```
GET https://connect.mindcloud.co/v1/universal/cATS/latest/actions/search-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cATS/latest/actions/search-jobs?connectionId=$CONNECTION_ID&query=MindCloud%20Stage%203%20Job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "MindCloud Stage 3 Job"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cATS/latest/actions/search-jobs?${params}`, {
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
| `query` | string | yes | The string to search within jobs for. Example: `MindCloud Stage 3 Job`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "Embedded": {
        "jobs": [
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
        ]
      },
      "Links": {
        "self": {
          "href": "https://example.com"
        }
      },
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `Embedded.jobs[].categoryName` | string |  |
| `Embedded.jobs[].companyId` | number |  |
| `Embedded.jobs[].contactId` | object |  |
| `Embedded.jobs[].countryCode` | object |  |
| `Embedded.jobs[].dateCreated` | string |  |
| `Embedded.jobs[].dateModified` | string |  |
| `Embedded.jobs[].departmentId` | object |  |
| `Embedded.jobs[].description` | object |  |
| `Embedded.jobs[].duration` | object |  |
| `Embedded.jobs[].Embedded.applications[].description` | string |  |
| `Embedded.jobs[].Embedded.applications[].Embedded.fields[].applicationId` | number |  |
| `Embedded.jobs[].Embedded.applications[].Embedded.fields[].comment` | string |  |
| `Embedded.jobs[].Embedded.applications[].Embedded.fields[].id` | number |  |
| `Embedded.jobs[].Embedded.applications[].Embedded.fields[].isRequired` | boolean |  |
| `Embedded.jobs[].Embedded.applications[].Embedded.fields[].linkedCustomFieldId` | object |  |
| `Embedded.jobs[].Embedded.applications[].Embedded.fields[].Links.self.href` | string |  |
| `Embedded.jobs[].Embedded.applications[].Embedded.fields[].minItems` | object |  |
| `Embedded.jobs[].Embedded.applications[].Embedded.fields[].position` | number |  |
| `Embedded.jobs[].Embedded.applications[].Embedded.fields[].savesToField` | string |  |
| `Embedded.jobs[].Embedded.applications[].Embedded.fields[].size` | object |  |
| `Embedded.jobs[].Embedded.applications[].Embedded.fields[].title` | string |  |
| `Embedded.jobs[].Embedded.applications[].Embedded.fields[].type` | string |  |
| `Embedded.jobs[].Embedded.applications[].header` | string |  |
| `Embedded.jobs[].Embedded.applications[].id` | number |  |
| `Embedded.jobs[].Embedded.applications[].Links.fields.href` | string |  |
| `Embedded.jobs[].Embedded.applications[].Links.self.href` | string |  |
| `Embedded.jobs[].Embedded.company.address.city` | object |  |
| `Embedded.jobs[].Embedded.company.address.postalCode` | object |  |
| `Embedded.jobs[].Embedded.company.address.state` | object |  |
| `Embedded.jobs[].Embedded.company.address.street` | object |  |
| `Embedded.jobs[].Embedded.company.billingContactId` | object |  |
| `Embedded.jobs[].Embedded.company.countryCode` | object |  |
| `Embedded.jobs[].Embedded.company.dateCreated` | string |  |
| `Embedded.jobs[].Embedded.company.dateModified` | string |  |
| `Embedded.jobs[].Embedded.company.enteredById` | number |  |
| `Embedded.jobs[].Embedded.company.id` | number |  |
| `Embedded.jobs[].Embedded.company.isHot` | boolean |  |
| `Embedded.jobs[].Embedded.company.keyTechnologies` | object |  |
| `Embedded.jobs[].Embedded.company.Links.self.href` | string |  |
| `Embedded.jobs[].Embedded.company.name` | string |  |
| `Embedded.jobs[].Embedded.company.notes` | string |  |
| `Embedded.jobs[].Embedded.company.ownerId` | number |  |
| `Embedded.jobs[].Embedded.company.phones.fax` | object |  |
| `Embedded.jobs[].Embedded.company.phones.primary` | object |  |
| `Embedded.jobs[].Embedded.company.phones.secondary` | object |  |
| `Embedded.jobs[].Embedded.company.statusId` | number |  |
| `Embedded.jobs[].Embedded.company.website` | object |  |
| `Embedded.jobs[].Embedded.status.id` | number |  |
| `Embedded.jobs[].Embedded.status.Links.self.href` | string |  |
| `Embedded.jobs[].Embedded.status.mapping` | string |  |
| `Embedded.jobs[].Embedded.status.title` | string |  |
| `Embedded.jobs[].Embedded.status.workflowId` | number |  |
| `Embedded.jobs[].externalId` | object |  |
| `Embedded.jobs[].id` | number |  |
| `Embedded.jobs[].isHot` | boolean |  |
| `Embedded.jobs[].isPublished` | boolean |  |
| `Embedded.jobs[].Links.applications.href` | string |  |
| `Embedded.jobs[].Links.attachments.href` | string |  |
| `Embedded.jobs[].Links.company.href` | string |  |
| `Embedded.jobs[].Links.customFields.href` | string |  |
| `Embedded.jobs[].Links.pipelines.href` | string |  |
| `Embedded.jobs[].Links.self.href` | string |  |
| `Embedded.jobs[].Links.status.href` | string |  |
| `Embedded.jobs[].Links.tags.href` | string |  |
| `Embedded.jobs[].location.city` | string |  |
| `Embedded.jobs[].location.postalCode` | string |  |
| `Embedded.jobs[].location.state` | string |  |
| `Embedded.jobs[].maxRate` | object |  |
| `Embedded.jobs[].notes` | object |  |
| `Embedded.jobs[].openings` | number |  |
| `Embedded.jobs[].ownerId` | number |  |
| `Embedded.jobs[].pipelineWorkflowId` | object |  |
| `Embedded.jobs[].portalHidden` | boolean |  |
| `Embedded.jobs[].recruiterId` | object |  |
| `Embedded.jobs[].remoteType` | object |  |
| `Embedded.jobs[].salary` | object |  |
| `Embedded.jobs[].sourcerId` | object |  |
| `Embedded.jobs[].startDate` | object |  |
| `Embedded.jobs[].statusId` | number |  |
| `Embedded.jobs[].title` | string |  |
| `Embedded.jobs[].type` | string |  |
| `Links.self.href` | string |  |
| `total` | number |  |

## Native endpoint

Through the native CATS API, this operation is `GET /jobs/search` (base URL `https://api.catsone.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-jobs.md) for the provider-specific parameters and requirements.

