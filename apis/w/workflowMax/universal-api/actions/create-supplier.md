# WorkflowMax: Create Supplier



```
POST https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/create-supplier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/create-supplier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/create-supplier', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



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
          "ccdInEmail": true,
          "createdAt": "string",
          "email": "ava@example.com",
          "firstName": "Ava",
          "lastName": "Chen",
          "mobile": "string",
          "phone": "string",
          "position": "string",
          "primary": true,
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
          "uploadedBy": "string",
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
| `addresses[].address` | string | The full address of the supplier address. |
| `addresses[].city` | string | The city of the supplier address. |
| `addresses[].country` | string | The country of the supplier address. |
| `addresses[].postalCode` | string | The postal code of the supplier address. |
| `addresses[].state` | string | The state of the supplier address. |
| `addresses[].street` | string | The street address of the supplier address. |
| `addresses[].type` | string | The type of the address, it could be billing or postal. |
| `contactDetails.email` | string | Primary email address of the supplier |
| `contactDetails.fax` | string | Fax number associated with the supplier |
| `contactDetails.phone` | string | Primary telephone number for the supplier |
| `contactDetails.website` | string | URL of the supplier’s official website |
| `contacts[].ccdInEmail` | boolean | Indicate whether email address to be CC’d on communications related to the supplier |
| `contacts[].createdAt` | string | The UTC timestamp indicating when the supplier contact record was created |
| `contacts[].email` | string | The supplier contact's primary email address used for communication and notifications |
| `contacts[].firstName` | string | The first name of the supplier contact. |
| `contacts[].lastName` | string | The last name or family name of the supplier’s contact person |
| `contacts[].mobile` | string | The mobile phone number of the supplier’s primary contact person |
| `contacts[].phone` | string | The landline or main phone number of the supplier’s primary contact person |
| `contacts[].position` | string | The job title or role of the supplier’s contact person within their organization |
| `contacts[].primary` | boolean | Boolean flag indicating whether the contact is the primary one |
| `contacts[].updatedAt` | string | The UTC timestamp of the last update made to the supplier contact record |
| `contacts[].uuid` | string | The unique identifier of the supplier contact. |
| `createdAt` | string | The UTC timestamp indicating when the supplier was created. |
| `customFields[].name` | string | The name of the custom field. |
| `customFields[].uuid` | string | The unique identifier of the custom field. |
| `customFields[].value` | string | The value of the custom field. |
| `deletedAt` | string | The UTC timestamp indicating when the supplier was deleted |
| `documents[].createdAt` | string | The UTC timestamp indicating when the document was created. |
| `documents[].downloadURL` | string | The download URL of the supplier document. |
| `documents[].fileName` | string | The file name of the supplier document. |
| `documents[].fileSize` | number | The size of the supplier document. |
| `documents[].note` | string | The note of the supplier document. |
| `documents[].phase` | string | The phase of the supplier document. |
| `documents[].title` | string | The title of the supplier document. |
| `documents[].updatedAt` | string | The UTC timestamp indicating when the document was last updated. |
| `documents[].uploadedBy` | string | The name of the staff who uploaded the supplier document. |
| `documents[].uuid` | string | The unique identifier of the supplier document. |
| `exportCode` | string | The export code of the supplier. |
| `favourite` | boolean | Indicate whether the supplier is marked as favourite. |
| `name` | string | The name of the supplier. |
| `notes[].comments[].comment` | string | The detail content of the comment. |
| `notes[].comments[].createdAt` | string | UTC timestamp indicating when the note comment was created. |
| `notes[].comments[].createdBy.firstName` | string | The first name of the staff who added comment to the supplier note. |
| `notes[].comments[].createdBy.lastName` | string | The last name of the staff who added comment to the supplier note. |
| `notes[].comments[].createdBy.uuid` | string | The unique identifier of the staff who added comment to the supplier note. |
| `notes[].comments[].updatedAt` | string | UTC timestamp indicating when the note comment was udpated. |
| `notes[].createdAt` | string | UTC timestamp indicating when the note was created. |
| `notes[].createdBy.firstName` | string | The first name of the staff who created this supplier note. |
| `notes[].createdBy.lastName` | string | The last name of the staff who created this supplier note. |
| `notes[].createdBy.uuid` | string | The unique identifier of the staff who created this supplier note. |
| `notes[].note` | string | The detail content of the supplier note. |
| `notes[].phase` | string | The phase of the supplier note. |
| `notes[].title` | string | The title of the supplier note. |
| `notes[].updatedAt` | string | UTC timestamp indicating when the note was updated. |
| `notes[].uuid` | string | The unique identifier of the supplier note. |
| `status` | string | Indicate whether the supplier is active or not. |
| `updatedAt` | string | The UTC timestamp indicates when the supplier was last updated. |
| `uuid` | string | The unique identifier of the supplier. |
| `zeroRatedGST[].rate` | number | It should be 0. |
| `zeroRatedGST[].tax_name` | string | The name of the zero rate tax. |

## Native endpoint

Through the native WorkflowMax API, this operation is `POST v2/suppliers` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-supplier.md) for the provider-specific parameters and requirements.

