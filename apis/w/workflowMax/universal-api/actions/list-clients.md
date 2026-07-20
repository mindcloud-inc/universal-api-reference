# WorkflowMax: List Clients



```
GET https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-clients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-clients?${params}`, {
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
            "billingClientUUID": "string",
            "businessStructureUUID": "string",
            "clientTypeUUID": "string",
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
          "clientManagerUUID": "string",
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
          "customFields": [
            {
              "name": "Ava Chen",
              "uuid": "string",
              "value": "string"
            }
          ],
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
              "uploadedByFirstName": "Ava",
              "uploadedByLastName": "Chen",
              "uuid": "string"
            }
          ],
          "exportCode": "string",
          "favorite": true,
          "jobManagerUUID": "string",
          "name": "Ava Chen",
          "notes": [
            {
              "createdAt": "string",
              "createdByFirstName": "Ava",
              "createdByLastName": "Chen",
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
          "updatedAt": "string",
          "uuid": "string"
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].addresses[].address` | string | The street address. |
| `data[].addresses[].city` | string | The city of the address. |
| `data[].addresses[].country` | string | The country of the address |
| `data[].addresses[].default` | boolean | Indicate whether this is the default address for the client. |
| `data[].addresses[].postalCode` | string | The postal code of the address. |
| `data[].addresses[].state` | string | The state of the address. |
| `data[].addresses[].type` | string | The type of the address, e.g. postal or billing. |
| `data[].archived` | boolean | Indicate whether the client is archived. |
| `data[].billingDetails.balanceDate` | string | The balance date of the client. |
| `data[].billingDetails.billingClientUUID` | string | The unique identifier of the client whose billing details is used for this client. It only returns when there is billing client assigned to the client. |
| `data[].billingDetails.businessStructureUUID` | string | The unique identifier of business structure of the client. It can be mapped with uuid in GET /businessStructures/ endpoint. |
| `data[].billingDetails.clientTypeUUID` | string | The unique identifier of client type of the client. It can be mapped with uuid in GET /clientTypes/ endpoint. |
| `data[].billingDetails.customRates[].billableRate` | number | The custom billable rate of the task for the client. |
| `data[].billingDetails.customRates[].taskUUID` | string | The unique identifier of the task that the client has custom rate. It can be mapped with uuid in GET /tasks/ endpoint. |
| `data[].billingDetails.invoiceDueDate` | string | The custom payment term of the client. |
| `data[].billingDetails.markup` | number | The markup percentage of the client. It is derived from the markup hierarchy in WorkflowMax, details please refer to https://support.workflowmax.com/hc/en-us/articles/24872327147289-Markup. |
| `data[].billingDetails.taxNumbers[].name` | string | The name of the tax |
| `data[].billingDetails.taxNumbers[].number` | string | The number of the tax. |
| `data[].billingDetails.zeroRatedTaxRate.rate` | number | The rate of the zero rated tax. |
| `data[].billingDetails.zeroRatedTaxRate.taxName` | string | The name of the zero rated tax. |
| `data[].clientGroups[].name` | string | The name of the group which the client belongs to. |
| `data[].clientGroups[].taxable` | boolean | Indicate whether the group is taxable. |
| `data[].clientGroups[].uuid` | string | The unique identifier of the group which the client belongs to. |
| `data[].clientManagerUUID` | string | The unique identifier of the client's client manager. |
| `data[].clientRelationships[].endDate` | string | The end date of the client relationship. |
| `data[].clientRelationships[].relatedClientUUID` | string | The unique identifier of the related client in this client relationship. |
| `data[].clientRelationships[].startDate` | string | The start date of the client relationship. |
| `data[].clientRelationships[].type` | string | The relationship type of the client relationship. |
| `data[].clientRelationships[].uuid` | string | The unique identifier of the client relationship. |
| `data[].contactDetails.email` | string | The email address of the client. |
| `data[].contactDetails.fax` | string | The fax number of the client. |
| `data[].contactDetails.phone` | string | The phone number of the client. |
| `data[].contactDetails.website` | string | The website of the client. |
| `data[].contacts[].firstName` | string | The first name of the contact. |
| `data[].contacts[].includeInEmails` | boolean | Indicate whether the contact needs to be included in the cc list in the email for the client. |
| `data[].contacts[].lastName` | string | The last name of the contact. |
| `data[].contacts[].position` | string | The position of the contact. |
| `data[].contacts[].primary` | boolean | Indicate whether the contact is primary contact for the client. |
| `data[].contacts[].salutation` | string | The salutation of the contact. |
| `data[].contacts[].uuid` | string | The unique identifier of the contact. |
| `data[].createdAt` | string | The UTC date and time when the client was created. |
| `data[].customFields[].name` | string | The name of the client custom field. |
| `data[].customFields[].uuid` | string | The unique identifier of the client custom field. |
| `data[].customFields[].value` | string | The value of the client custom field. |
| `data[].documents[].createdAt` | string | The UTC date and time when the client document was created. |
| `data[].documents[].downloadURL` | string | The download URL of the client document. |
| `data[].documents[].fileName` | string | The file name of the client document. |
| `data[].documents[].fileSize` | number | The file size of the client document. |
| `data[].documents[].note` | string | The note detail of the client document. |
| `data[].documents[].phase` | string | The phase of the client document. |
| `data[].documents[].title` | string | The title of the client document. |
| `data[].documents[].updatedAt` | string | The UTC date and time when the client document was last updated. |
| `data[].documents[].uploadedByFirstName` | string | The first name of the staff who uploaded the client document. |
| `data[].documents[].uploadedByLastName` | string | The last name of the staff who uploaded the client document. |
| `data[].documents[].uuid` | string | The unique identifier of the client document. |
| `data[].exportCode` | string | The export code of the client. |
| `data[].favorite` | boolean | Indicate whether the client is marked as favorite. |
| `data[].jobManagerUUID` | string | The unique identifier of the client's job manager. |
| `data[].name` | string | The name of the client. When business structure is individual, the name is first name + last name. |
| `data[].notes[].createdAt` | string | The UTC date and time when the client note was created. |
| `data[].notes[].createdByFirstName` | string | The first name of the staff who created the client note. |
| `data[].notes[].createdByLastName` | string | The last name of the staff who created the client note. |
| `data[].notes[].date` | string | The UTC date of the client note. |
| `data[].notes[].description` | string | The description of the client note. |
| `data[].notes[].phase` | string | The phase of the client note. |
| `data[].notes[].title` | string | The title of the client note. |
| `data[].notes[].updatedAt` | string | The UTC date and time when the client was last updated. |
| `data[].notes[].uuid` | string | The unique identifier of the client note. |
| `data[].prospect` | boolean | Indicate whether the client is a prospect. The client is a prospect if it has leads and no won leads yet. |
| `data[].referralSource` | string | The referral source of the client. |
| `data[].updatedAt` | string | The UTC date and time when the client was last updated |
| `data[].uuid` | string | The unique identifier of the client. |
| `total` | number |  |

## Native endpoint

Through the native WorkflowMax API, this operation is `GET v2/clients` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

