# WorkflowMax: Get Supplier



```
GET https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-supplier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-supplier?connectionId=$CONNECTION_ID&supplierId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "supplierId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-supplier?${params}`, {
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
| `supplierId` | string | yes | The WorkflowMax supplier UUID. |

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
          "postalCode": "string",
          "state": "string",
          "street": "string",
          "type": "string"
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
          "createdAt": "string",
          "email": "ava@example.com",
          "firstName": "Ava",
          "lastName": "Chen",
          "mobile": "string",
          "phone": "string",
          "position": "string",
          "updatedAt": "string",
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
      "deletedAt": "string",
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
      "favourite": true,
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
          "note": "string",
          "phase": "string",
          "title": "string",
          "updatedAt": "string",
          "uuid": "string"
        }
      ],
      "status": "string",
      "updatedAt": "string",
      "uuid": "string",
      "zeroRatedGST": [
        {
          "rate": 1,
          "tax_name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses[].address` | string | The details of the address. |
| `addresses[].city` | string | The city information of the address. |
| `addresses[].country` | string | The country information of the address. |
| `addresses[].postalCode` | string | The postal code information of the address. |
| `addresses[].state` | string | The state information of the address. |
| `addresses[].street` | string | The street information of the address. |
| `addresses[].type` | string | The type of the address, e.g. physical or postal. |
| `contactDetails.email` | string | The email address of the supplier. |
| `contactDetails.fax` | string | The fax number of the supplier. |
| `contactDetails.phone` | string | The phone number of the supplier. |
| `contactDetails.website` | string | The website of the supplier. |
| `contacts[].createdAt` | string | The date and time when the supplier contact was created. |
| `contacts[].email` | string | The email address of the supplier contact. |
| `contacts[].firstName` | string | The first name of the supplier contact. |
| `contacts[].lastName` | string | The last name of the supplier contact. |
| `contacts[].mobile` | string | The mobile number of the supplier contact. |
| `contacts[].phone` | string | The phone number of the supplier contact. |
| `contacts[].position` | string | The position of the supplier contact. |
| `contacts[].updatedAt` | string | The date and time when the supplier contact was last updated. |
| `contacts[].uuid` | string | The unique identifier of the supplier contact. |
| `createdAt` | string | The UTC date and time when the supplier was created. |
| `customFields[].name` | string | The name of the custom field. |
| `customFields[].uuid` | string | The unique identifier of the custom field. |
| `customFields[].value` | string | The value of the custom field. |
| `deletedAt` | string | The UTC date and time when the supplier was deleted. It only populate when the supplier was deleted. |
| `documents[].createdAt` | string | The UTC date and time when the document was created. |
| `documents[].downloadURL` | string | The download URL of the document. |
| `documents[].fileName` | string | The file name of the document. |
| `documents[].fileSize` | number | The file size of the document. |
| `documents[].note` | string | The note of the document. |
| `documents[].phase` | string | The phase name of the document. |
| `documents[].title` | string | The title of the document. |
| `documents[].updatedAt` | string | The UTC date and time when the document was last updated. |
| `documents[].uploadedBy.firstName` | string | The first name of the staff who updated the document. |
| `documents[].uploadedBy.lastName` | string | The last name of the staff who updated the document. |
| `documents[].uploadedBy.uuid` | string | The unique identifier of the staff who updated the document. |
| `documents[].uuid` | string | The unique identifier of the document. |
| `exportCode` | string | The export code of the supplier. |
| `favourite` | boolean | Indicate whether the supplier is marked as favourite. |
| `name` | string | The name of the supplier. |
| `notes[].comments[].comment` | string | The detail of the comment. |
| `notes[].comments[].createdAt` | string | The date and time when the comment was created. |
| `notes[].comments[].createdBy.firstName` | string | The first name of the staff who created the comment. |
| `notes[].comments[].createdBy.lastName` | string | The last name of the staff who created the comment. |
| `notes[].comments[].createdBy.uuid` | string | The unique identifier of the staff who created the comment. |
| `notes[].comments[].updatedAt` | string | The date and time when the comment was last updated. |
| `notes[].createdAt` | string | The UTC date and time when the note was created. |
| `notes[].createdBy.firstName` | string | The first name of the staff who created the note. |
| `notes[].createdBy.lastName` | string | The last name of the staff who created the note. |
| `notes[].createdBy.uuid` | string | The unique identifier of the staff who created the note. |
| `notes[].note` | string | The note details of the note. |
| `notes[].phase` | string | The phase name of the note. |
| `notes[].title` | string | The title of the note. |
| `notes[].updatedAt` | string | The UTC date and time when the note was last upated. |
| `notes[].uuid` | string | The unique identifier of the note. |
| `status` | string | The status of the supplier, e.g. active, archived, deleted. |
| `updatedAt` | string | The UTC date and time when the supplier was last updated. |
| `uuid` | string | The unique identifier of the supplier. |
| `zeroRatedGST[].rate` | number | The rate of the zero rated tax, it should always be 0. |
| `zeroRatedGST[].tax_name` | string | The name of the zero rated tax. |

## Native endpoint

Through the native WorkflowMax API, this operation is `GET v2/suppliers/{UUID}` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-supplier.md) for the provider-specific parameters and requirements.

