# Recruitee ATS: Delete Offer



```
DELETE https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/delete-offer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recruitee ATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/delete-offer?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recruiteeATS/latest/actions/delete-offer?${params}`, {
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
| `id` | number | yes | Offer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "offer": {
        "adminappUrl": "https://example.com",
        "attachmentsCount": 1,
        "autoReplyTemplateId": 1,
        "candidatesCount": 1,
        "careersJobPageLayoutId": 1,
        "careersUrl": "https://example.com",
        "category": {},
        "city": {},
        "closedAt": {},
        "countryCode": {},
        "coverImage": {},
        "coverImageUrl": {},
        "createdAt": "string",
        "defaultTranslations": {
          "description": "string",
          "descriptionHtml": "string",
          "descriptionJson": {
            "doc": {
              "content": [
                {
                  "attrs": {
                    "align": "string",
                    "htmlClass": "string"
                  },
                  "content": [
                    {
                      "text": "string",
                      "type": "string"
                    }
                  ],
                  "type": "string"
                }
              ],
              "type": "string"
            }
          },
          "emailConfirmationBody": "ava@example.com",
          "emailConfirmationSubject": "ava@example.com",
          "locationsQuestion": "string",
          "title": "string"
        },
        "department": {},
        "departmentId": {},
        "description": "string",
        "descriptionHtml": "string",
        "descriptionJson": {
          "doc": {
            "content": [
              {
                "attrs": {
                  "align": "string",
                  "htmlClass": "string"
                },
                "content": [
                  {
                    "text": "string",
                    "type": "string"
                  }
                ],
                "type": "string"
              }
            ],
            "type": "string"
          }
        },
        "disqualifiedCandidatesCount": 1,
        "dynamicFieldsCount": 1,
        "education": {},
        "eeoSettings": {},
        "emailConfirmation": true,
        "emailConfirmationBody": "ava@example.com",
        "emailConfirmationSubject": "ava@example.com",
        "employmentType": {},
        "enabledForReferrals": true,
        "example": true,
        "experience": {},
        "fieldset": {
          "default": true,
          "fields": [
            {
              "id": 1,
              "kind": "string",
              "name": "Ava Chen",
              "visibility": {
                "level": "string"
              },
              "visible": true
            }
          ],
          "id": 1,
          "name": "Ava Chen"
        },
        "fieldsetId": 1,
        "followed": true,
        "guid": "string",
        "hasActiveCampaign": true,
        "hasAdditionalInfo": true,
        "hasAutomations": true,
        "highlightHtml": {},
        "highlightJson": {},
        "hireAssistant": {},
        "hiredCandidatesCount": 1,
        "hiredCandidatesWithoutOpeningsCount": {},
        "hiringManagerId": {},
        "hybrid": true,
        "id": 1,
        "issues": {
          "isDynamicFieldsLimitExceeded": true,
          "isMigratedHtmlEqual": {},
          "isRequiredDataMissing": true,
          "isRequisitionMissing": true
        },
        "jobScheduler": {},
        "kind": "string",
        "langCode": "string",
        "location": {},
        "locationsQuestion": "string",
        "locationsQuestionRequired": true,
        "locationsQuestionType": "string",
        "mailboxEmail": "ava@example.com",
        "maxHours": {},
        "maxHoursPerWeek": {},
        "minHours": {},
        "minHoursPerWeek": {},
        "notesCount": 1,
        "numberOfOpenings": {},
        "onSite": true,
        "openQuestionTemplateId": {},
        "optionsCoverLetter": "string",
        "optionsCv": "string",
        "optionsPhone": "string",
        "optionsPhoto": "string",
        "optionsSalutation": "string",
        "optionsTitle": "string",
        "pipeline": true,
        "pipelineTemplate": {
          "category": {},
          "custom": true,
          "default": true,
          "id": 1,
          "position": {},
          "requiresAdjustment": true,
          "stages": [
            {
              "candidateAnonymizationEnabled": true,
              "category": "string",
              "fairEvaluationsEnabled": true,
              "group": "string",
              "id": 1,
              "locked": true,
              "name": "Ava Chen",
              "placementsCount": 1,
              "position": 1,
              "timeLimit": {}
            }
          ],
          "title": "string"
        },
        "pipelineTemplateId": 1,
        "position": 1,
        "postalCode": {},
        "primaryLangCode": "string",
        "priority": {},
        "publishedAt": {},
        "qualifiedCandidatesCount": 1,
        "recruiterId": {},
        "remote": true,
        "requirements": "string",
        "requirementsHtml": "string",
        "requirementsJson": {
          "doc": {
            "content": [
              {
                "attrs": {
                  "align": "string",
                  "htmlClass": "string"
                },
                "content": [
                  {
                    "text": "string",
                    "type": "string"
                  }
                ],
                "type": "string"
              }
            ],
            "type": "string"
          }
        },
        "salary": {
          "currency": {},
          "max": {},
          "min": {},
          "period": {}
        },
        "sharedOpeningsCount": {},
        "sharingDescription": {},
        "sharingImage": {},
        "sharingImageUrl": {},
        "sharingTitle": {},
        "slug": "string",
        "stateCode": {},
        "stateName": {},
        "status": "string",
        "street": {},
        "title": "string",
        "updatedAt": "string",
        "url": "https://example.com",
        "visibilityOptions": [
          "string"
        ],
        "wysiwygEditor": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `offer.adminappUrl` | string |  |
| `offer.attachmentsCount` | number |  |
| `offer.autoReplyTemplateId` | number |  |
| `offer.candidatesCount` | number |  |
| `offer.careersJobPageLayoutId` | number |  |
| `offer.careersUrl` | string |  |
| `offer.category` | object |  |
| `offer.city` | object |  |
| `offer.closedAt` | object |  |
| `offer.countryCode` | object |  |
| `offer.coverImage` | object |  |
| `offer.coverImageUrl` | object |  |
| `offer.createdAt` | string |  |
| `offer.defaultTranslations.description` | string |  |
| `offer.defaultTranslations.descriptionHtml` | string |  |
| `offer.defaultTranslations.descriptionJson.doc.content[].attrs.align` | string |  |
| `offer.defaultTranslations.descriptionJson.doc.content[].attrs.htmlClass` | string |  |
| `offer.defaultTranslations.descriptionJson.doc.content[].content[].text` | string |  |
| `offer.defaultTranslations.descriptionJson.doc.content[].content[].type` | string |  |
| `offer.defaultTranslations.descriptionJson.doc.content[].type` | string |  |
| `offer.defaultTranslations.descriptionJson.doc.type` | string |  |
| `offer.defaultTranslations.emailConfirmationBody` | string |  |
| `offer.defaultTranslations.emailConfirmationSubject` | string |  |
| `offer.defaultTranslations.locationsQuestion` | string |  |
| `offer.defaultTranslations.title` | string |  |
| `offer.department` | object |  |
| `offer.departmentId` | object |  |
| `offer.description` | string |  |
| `offer.descriptionHtml` | string |  |
| `offer.descriptionJson.doc.content[].attrs.align` | string |  |
| `offer.descriptionJson.doc.content[].attrs.htmlClass` | string |  |
| `offer.descriptionJson.doc.content[].content[].text` | string |  |
| `offer.descriptionJson.doc.content[].content[].type` | string |  |
| `offer.descriptionJson.doc.content[].type` | string |  |
| `offer.descriptionJson.doc.type` | string |  |
| `offer.disqualifiedCandidatesCount` | number |  |
| `offer.dynamicFieldsCount` | number |  |
| `offer.education` | object |  |
| `offer.eeoSettings` | object |  |
| `offer.emailConfirmation` | boolean |  |
| `offer.emailConfirmationBody` | string |  |
| `offer.emailConfirmationSubject` | string |  |
| `offer.employmentType` | object |  |
| `offer.enabledForReferrals` | boolean |  |
| `offer.example` | boolean |  |
| `offer.experience` | object |  |
| `offer.fieldset.default` | boolean |  |
| `offer.fieldset.fields[].id` | number |  |
| `offer.fieldset.fields[].kind` | string |  |
| `offer.fieldset.fields[].name` | string |  |
| `offer.fieldset.fields[].visibility.level` | string |  |
| `offer.fieldset.fields[].visible` | boolean |  |
| `offer.fieldset.id` | number |  |
| `offer.fieldset.name` | string |  |
| `offer.fieldsetId` | number |  |
| `offer.followed` | boolean |  |
| `offer.guid` | string |  |
| `offer.hasActiveCampaign` | boolean |  |
| `offer.hasAdditionalInfo` | boolean |  |
| `offer.hasAutomations` | boolean |  |
| `offer.highlightHtml` | object |  |
| `offer.highlightJson` | object |  |
| `offer.hireAssistant` | object |  |
| `offer.hiredCandidatesCount` | number |  |
| `offer.hiredCandidatesWithoutOpeningsCount` | object |  |
| `offer.hiringManagerId` | object |  |
| `offer.hybrid` | boolean |  |
| `offer.id` | number |  |
| `offer.issues.isDynamicFieldsLimitExceeded` | boolean |  |
| `offer.issues.isMigratedHtmlEqual` | object |  |
| `offer.issues.isRequiredDataMissing` | boolean |  |
| `offer.issues.isRequisitionMissing` | boolean |  |
| `offer.jobScheduler` | object |  |
| `offer.kind` | string |  |
| `offer.langCode` | string |  |
| `offer.location` | object |  |
| `offer.locationsQuestion` | string |  |
| `offer.locationsQuestionRequired` | boolean |  |
| `offer.locationsQuestionType` | string |  |
| `offer.mailboxEmail` | string |  |
| `offer.maxHours` | object |  |
| `offer.maxHoursPerWeek` | object |  |
| `offer.minHours` | object |  |
| `offer.minHoursPerWeek` | object |  |
| `offer.notesCount` | number |  |
| `offer.numberOfOpenings` | object |  |
| `offer.onSite` | boolean |  |
| `offer.openQuestionTemplateId` | object |  |
| `offer.optionsCoverLetter` | string |  |
| `offer.optionsCv` | string |  |
| `offer.optionsPhone` | string |  |
| `offer.optionsPhoto` | string |  |
| `offer.optionsSalutation` | string |  |
| `offer.optionsTitle` | string |  |
| `offer.pipeline` | boolean |  |
| `offer.pipelineTemplate.category` | object |  |
| `offer.pipelineTemplate.custom` | boolean |  |
| `offer.pipelineTemplate.default` | boolean |  |
| `offer.pipelineTemplate.id` | number |  |
| `offer.pipelineTemplate.position` | object |  |
| `offer.pipelineTemplate.requiresAdjustment` | boolean |  |
| `offer.pipelineTemplate.stages[].candidateAnonymizationEnabled` | boolean |  |
| `offer.pipelineTemplate.stages[].category` | string |  |
| `offer.pipelineTemplate.stages[].fairEvaluationsEnabled` | boolean |  |
| `offer.pipelineTemplate.stages[].group` | string |  |
| `offer.pipelineTemplate.stages[].id` | number |  |
| `offer.pipelineTemplate.stages[].locked` | boolean |  |
| `offer.pipelineTemplate.stages[].name` | string |  |
| `offer.pipelineTemplate.stages[].placementsCount` | number |  |
| `offer.pipelineTemplate.stages[].position` | number |  |
| `offer.pipelineTemplate.stages[].timeLimit` | object |  |
| `offer.pipelineTemplate.title` | string |  |
| `offer.pipelineTemplateId` | number |  |
| `offer.position` | number |  |
| `offer.postalCode` | object |  |
| `offer.primaryLangCode` | string |  |
| `offer.priority` | object |  |
| `offer.publishedAt` | object |  |
| `offer.qualifiedCandidatesCount` | number |  |
| `offer.recruiterId` | object |  |
| `offer.remote` | boolean |  |
| `offer.requirements` | string |  |
| `offer.requirementsHtml` | string |  |
| `offer.requirementsJson.doc.content[].attrs.align` | string |  |
| `offer.requirementsJson.doc.content[].attrs.htmlClass` | string |  |
| `offer.requirementsJson.doc.content[].content[].text` | string |  |
| `offer.requirementsJson.doc.content[].content[].type` | string |  |
| `offer.requirementsJson.doc.content[].type` | string |  |
| `offer.requirementsJson.doc.type` | string |  |
| `offer.salary.currency` | object |  |
| `offer.salary.max` | object |  |
| `offer.salary.min` | object |  |
| `offer.salary.period` | object |  |
| `offer.sharedOpeningsCount` | object |  |
| `offer.sharingDescription` | object |  |
| `offer.sharingImage` | object |  |
| `offer.sharingImageUrl` | object |  |
| `offer.sharingTitle` | object |  |
| `offer.slug` | string |  |
| `offer.stateCode` | object |  |
| `offer.stateName` | object |  |
| `offer.status` | string |  |
| `offer.street` | object |  |
| `offer.title` | string |  |
| `offer.updatedAt` | string |  |
| `offer.url` | string |  |
| `offer.visibilityOptions[]` | string |  |
| `offer.wysiwygEditor` | string |  |

## Native endpoint

Through the native Recruitee ATS API, this operation is `DELETE /c/:company_id/offers/:id` (base URL `https://api.recruitee.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-offer.md) for the provider-specific parameters and requirements.

