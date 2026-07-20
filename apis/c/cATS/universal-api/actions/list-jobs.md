# CATS: List Jobs

Retrieves jobs from the CATS account.

```
GET https://connect.mindcloud.co/v1/universal/cATS/latest/actions/list-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CATS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cATS/latest/actions/list-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cATS/latest/actions/list-jobs?${params}`, {
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
      "count": 1,
      "Embedded": {
        "jobs": [
          {
            "categoryName": "Ava Chen",
            "companyId": 1,
            "contactId": 1,
            "countryCode": {},
            "dateCreated": "string",
            "dateModified": "string",
            "departmentId": {},
            "description": "string",
            "duration": "string",
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
                  "city": "string",
                  "postalCode": "string",
                  "state": "string",
                  "street": "string"
                },
                "billingContactId": {},
                "countryCode": {},
                "dateCreated": "string",
                "dateModified": "string",
                "enteredById": 1,
                "id": 1,
                "isHot": true,
                "keyTechnologies": "string",
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
                "website": "string"
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
            "externalId": "string",
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
              "owner": {
                "href": "https://example.com"
              },
              "pipelines": {
                "href": "https://example.com"
              },
              "recruiter": {
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
            "maxRate": "string",
            "notes": "string",
            "openings": 1,
            "ownerId": 1,
            "pipelineWorkflowId": 1,
            "portalHidden": true,
            "recruiterId": 1,
            "remoteType": {},
            "salary": "string",
            "sourcerId": {},
            "startDate": "string",
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
| `Embedded.jobs[].contactId` | number |  |
| `Embedded.jobs[].countryCode` | object |  |
| `Embedded.jobs[].dateCreated` | string |  |
| `Embedded.jobs[].dateModified` | string |  |
| `Embedded.jobs[].departmentId` | object |  |
| `Embedded.jobs[].description` | string |  |
| `Embedded.jobs[].duration` | string |  |
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
| `Embedded.jobs[].Embedded.company.address.city` | string |  |
| `Embedded.jobs[].Embedded.company.address.postalCode` | string |  |
| `Embedded.jobs[].Embedded.company.address.state` | string |  |
| `Embedded.jobs[].Embedded.company.address.street` | string |  |
| `Embedded.jobs[].Embedded.company.billingContactId` | object |  |
| `Embedded.jobs[].Embedded.company.countryCode` | object |  |
| `Embedded.jobs[].Embedded.company.dateCreated` | string |  |
| `Embedded.jobs[].Embedded.company.dateModified` | string |  |
| `Embedded.jobs[].Embedded.company.enteredById` | number |  |
| `Embedded.jobs[].Embedded.company.id` | number |  |
| `Embedded.jobs[].Embedded.company.isHot` | boolean |  |
| `Embedded.jobs[].Embedded.company.keyTechnologies` | string |  |
| `Embedded.jobs[].Embedded.company.Links.self.href` | string |  |
| `Embedded.jobs[].Embedded.company.name` | string |  |
| `Embedded.jobs[].Embedded.company.notes` | string |  |
| `Embedded.jobs[].Embedded.company.ownerId` | number |  |
| `Embedded.jobs[].Embedded.company.phones.fax` | object |  |
| `Embedded.jobs[].Embedded.company.phones.primary` | object |  |
| `Embedded.jobs[].Embedded.company.phones.secondary` | object |  |
| `Embedded.jobs[].Embedded.company.statusId` | number |  |
| `Embedded.jobs[].Embedded.company.website` | string |  |
| `Embedded.jobs[].Embedded.status.id` | number |  |
| `Embedded.jobs[].Embedded.status.Links.self.href` | string |  |
| `Embedded.jobs[].Embedded.status.mapping` | string |  |
| `Embedded.jobs[].Embedded.status.title` | string |  |
| `Embedded.jobs[].Embedded.status.workflowId` | number |  |
| `Embedded.jobs[].externalId` | string |  |
| `Embedded.jobs[].id` | number |  |
| `Embedded.jobs[].isHot` | boolean |  |
| `Embedded.jobs[].isPublished` | boolean |  |
| `Embedded.jobs[].Links.applications.href` | string |  |
| `Embedded.jobs[].Links.attachments.href` | string |  |
| `Embedded.jobs[].Links.company.href` | string |  |
| `Embedded.jobs[].Links.customFields.href` | string |  |
| `Embedded.jobs[].Links.owner.href` | string |  |
| `Embedded.jobs[].Links.pipelines.href` | string |  |
| `Embedded.jobs[].Links.recruiter.href` | string |  |
| `Embedded.jobs[].Links.self.href` | string |  |
| `Embedded.jobs[].Links.status.href` | string |  |
| `Embedded.jobs[].Links.tags.href` | string |  |
| `Embedded.jobs[].location.city` | string |  |
| `Embedded.jobs[].location.postalCode` | string |  |
| `Embedded.jobs[].location.state` | string |  |
| `Embedded.jobs[].maxRate` | string |  |
| `Embedded.jobs[].notes` | string |  |
| `Embedded.jobs[].openings` | number |  |
| `Embedded.jobs[].ownerId` | number |  |
| `Embedded.jobs[].pipelineWorkflowId` | number |  |
| `Embedded.jobs[].portalHidden` | boolean |  |
| `Embedded.jobs[].recruiterId` | number |  |
| `Embedded.jobs[].remoteType` | object |  |
| `Embedded.jobs[].salary` | string |  |
| `Embedded.jobs[].sourcerId` | object |  |
| `Embedded.jobs[].startDate` | string |  |
| `Embedded.jobs[].statusId` | number |  |
| `Embedded.jobs[].title` | string |  |
| `Embedded.jobs[].type` | string |  |
| `Links.self.href` | string |  |
| `total` | number |  |

## Native endpoint

Through the native CATS API, this operation is `GET /jobs` (base URL `https://api.catsone.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-jobs.md) for the provider-specific parameters and requirements.

