# WorkflowMax: Get Client



```
GET https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-client?connectionId=$CONNECTION_ID&clientId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-client?${params}`, {
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
| `clientId` | string | yes | The WorkflowMax client UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {
          "address": "string",
          "city": "string",
          "country": "string",
          "default": true,
          "postalCode": "string",
          "state": "string",
          "type": "string"
        }
      ],
      "archived": true,
      "billingDetails": {
        "balanceDate": "string",
        "billingClient": {
          "name": "Ava Chen",
          "uuid": "string"
        },
        "businessStructure": {
          "name": "Ava Chen",
          "uuid": "string"
        },
        "clientType": {
          "clientType": "string",
          "uuid": "string"
        },
        "customRates": [
          {
            "billableRate": 1,
            "taskUUID": "string"
          }
        ],
        "invoiceDueDate": "string",
        "markup": 1,
        "taxNumbers": [
          {
            "name": "Ava Chen",
            "number": "string"
          }
        ],
        "zeroRatedTaxRate": {
          "rate": 1,
          "taxName": "Ava Chen"
        }
      },
      "clientGroups": [
        {
          "name": "Ava Chen",
          "taxable": true,
          "uuid": "string"
        }
      ],
      "clientManager": {
        "firstName": "Ava",
        "lastName": "Chen",
        "uuid": "string"
      },
      "clientRelationships": [
        {
          "endDate": "string",
          "relatedClientUUID": "string",
          "startDate": "string",
          "type": "string",
          "uuid": "string"
        }
      ],
      "contactDetails": {
        "email": "ava@example.com",
        "fax": "string",
        "phone": "string",
        "website": "string"
      },
      "contacts": [
        {
          "firstName": "Ava",
          "includeInEmails": true,
          "lastName": "Chen",
          "position": "string",
          "primary": true,
          "salutation": "string",
          "uuid": "string"
        }
      ],
      "createdAt": "string",
      "customFields": {
        "4": {
          "name": "Ava Chen",
          "uuid": "string",
          "value": "string"
        }
      },
      "documents": [
        {
          "createdAt": "string",
          "downloadURL": "https://example.com",
          "fileName": "Ava Chen",
          "fileSize": 1,
          "note": "string",
          "phase": "string",
          "title": "string",
          "updatedAt": "string",
          "uploadedBy": {
            "firstName": "Ava",
            "lastName": "Chen",
            "uuid": "string"
          },
          "uuid": "string"
        }
      ],
      "exportCode": "string",
      "favorite": true,
      "jobManager": {
        "firstName": "Ava",
        "lastName": "Chen",
        "uuid": "string"
      },
      "modifiedAt": "string",
      "name": "Ava Chen",
      "notes": [
        {
          "comments": [
            {
              "comment": "string",
              "createdAt": "string",
              "createdBy": {
                "firstName": "Ava",
                "lastName": "Chen",
                "uuid": "string"
              },
              "updatedAt": "string"
            }
          ],
          "createdAt": "string",
          "createdBy": {
            "firstName": "Ava",
            "lastName": "Chen",
            "uuid": "string"
          },
          "date": "string",
          "description": "string",
          "phase": "string",
          "title": "string",
          "updatedAt": "string",
          "uuid": "string"
        }
      ],
      "prospect": true,
      "referralSource": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses[].address` | string | The street address. |
| `addresses[].city` | string | The city of the address. |
| `addresses[].country` | string | The country of the address |
| `addresses[].default` | boolean | Indicate whether this is the default address for the client. |
| `addresses[].postalCode` | string | The postal code of the address. |
| `addresses[].state` | string | The state of the address. |
| `addresses[].type` | string | The type of the address, e.g. postal or billing. |
| `archived` | boolean | Indicate whether the client is archived. |
| `billingDetails.balanceDate` | string | The balance date of the client. |
| `billingDetails.billingClient.name` | string | The name of the client whose billing details is used for this client. |
| `billingDetails.billingClient.uuid` | string | The unique identifier of the client whose billing details is used for this client. |
| `billingDetails.businessStructure.name` | string | The name of business structure of the client. |
| `billingDetails.businessStructure.uuid` | string | The unique identifier of business structure of the client. |
| `billingDetails.clientType.clientType` | string | The name of client type of the client. |
| `billingDetails.clientType.uuid` | string | The unique identifier of client type of the client. |
| `billingDetails.customRates[].billableRate` | number | The custom billable rate of the task for the client. |
| `billingDetails.customRates[].taskUUID` | string |  |
| `billingDetails.invoiceDueDate` | string | The custom payment term of the client. |
| `billingDetails.markup` | number | The markup percentage of the client. It is derived from the markup hierarchy in WorkflowMax, details please refer to https://support.workflowmax.com/hc/en-us/articles/24872327147289-Markup. |
| `billingDetails.taxNumbers[].name` | string | The name of the tax |
| `billingDetails.taxNumbers[].number` | string | The number of the tax. |
| `billingDetails.zeroRatedTaxRate.rate` | number | The rate of the zero rated tax. |
| `billingDetails.zeroRatedTaxRate.taxName` | string | The name of the zero rated tax. |
| `clientGroups[].name` | string | The name of the group which the client belongs to. |
| `clientGroups[].taxable` | boolean | Indicate whether the group is taxable. |
| `clientGroups[].uuid` | string | The unique identifier of the group which the client belongs to. |
| `clientManager.firstName` | string | The first name of the client's client manager. |
| `clientManager.lastName` | string | The last name of the client's client manager. |
| `clientManager.uuid` | string | The unique identifier of the client's client manager. |
| `clientRelationships[].endDate` | string | The end date of the client relationship. |
| `clientRelationships[].relatedClientUUID` | string | The unique identifier of the related client in this client relationship. |
| `clientRelationships[].startDate` | string | The start date of the client relationship. |
| `clientRelationships[].type` | string | The relationship type of the client relationship. |
| `clientRelationships[].uuid` | string | The unique identifier of the client relationship. |
| `contactDetails.email` | string | The email address of the client. |
| `contactDetails.fax` | string | The fax number of the client. |
| `contactDetails.phone` | string | The phone number of the client. |
| `contactDetails.website` | string | The website of the client. |
| `contacts[].firstName` | string | The first name of the contact. |
| `contacts[].includeInEmails` | boolean | Indicate whether the contact needs to be included in the cc list in the email for the client. |
| `contacts[].lastName` | string | The last name of the contact. |
| `contacts[].position` | string | The position of the contact. |
| `contacts[].primary` | boolean | Indicate whether the contact is primary contact for the client. |
| `contacts[].salutation` | string | The salutation of the contact. |
| `contacts[].uuid` | string | The unique identifier of the contact. |
| `createdAt` | string | The UTC date and time when the client was created. |
| `customFields.4.name` | string | The name of the client custom field. |
| `customFields.4.uuid` | string | The unique identifier of the client custom field. |
| `customFields.4.value` | string | The value of the client custom field. |
| `documents[].createdAt` | string | The UTC date and time when the client document was created. |
| `documents[].downloadURL` | string | The download URL of the client document. |
| `documents[].fileName` | string | The file name of the client document. |
| `documents[].fileSize` | number | The file size of the client document. |
| `documents[].note` | string | The note detail of the client document. |
| `documents[].phase` | string | The phase of the client document. |
| `documents[].title` | string | The title of the client document. |
| `documents[].updatedAt` | string | The UTC date and time when the client document was last updated. |
| `documents[].uploadedBy.firstName` | string | The first name of the staff who uploaded the client document. |
| `documents[].uploadedBy.lastName` | string | The first name of the staff who uploaded the client document. |
| `documents[].uploadedBy.uuid` | string | The unique identifier of the staff who uploaded the client document. |
| `documents[].uuid` | string | The unique identifier of the client document. |
| `exportCode` | string | The export code of the client. |
| `favorite` | boolean | Indicate whether the client is marked as favorite. |
| `jobManager.firstName` | string | The first name of the client's job manager. |
| `jobManager.lastName` | string | The last name of the client's job manager. |
| `jobManager.uuid` | string | The unique identifier of the client's job manager. |
| `modifiedAt` | string | The UTC date and time when the client was last updated |
| `name` | string | The name of the client. When business structure is individual, the name is first name + last name. |
| `notes[].comments[].comment` | string | The detail of the client note comment. |
| `notes[].comments[].createdAt` | string | The date and time when the client note comment was created. |
| `notes[].comments[].createdBy.firstName` | string | The first name of the staff who created the client note comment. |
| `notes[].comments[].createdBy.lastName` | string | The last name of the staff who created the client note comment. |
| `notes[].comments[].createdBy.uuid` | string | The unique identifier of the staff who created the client note comment. |
| `notes[].comments[].updatedAt` | string | The date and time when the client note comment was last updated. |
| `notes[].createdAt` | string | The UTC date and time when the client note was created. |
| `notes[].createdBy.firstName` | string | The first name of the staff who created the client note. |
| `notes[].createdBy.lastName` | string | The last name of the staff who created the client note. |
| `notes[].createdBy.uuid` | string | The unique identifier of the staff who created the client note. |
| `notes[].date` | string | The UTC date of the client note. |
| `notes[].description` | string | The description of the client note. |
| `notes[].phase` | string | The phase of the client note. |
| `notes[].title` | string | The title of the client note. |
| `notes[].updatedAt` | string | The UTC date and time when the client was last updated. |
| `notes[].uuid` | string | The unique identifier of the client note. |
| `prospect` | boolean | Indicate whether the client is a prospect. The client is a prospect if it has leads and no won leads yet. |
| `referralSource` | string | The referral source of the client. |
| `uuid` | string | The unique identifier of the client. |

## Native endpoint

Through the native WorkflowMax API, this operation is `GET v2/clients/{UUID}` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

