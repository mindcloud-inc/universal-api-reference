# WorkflowMax: List Suppliers



```
GET https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-suppliers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-suppliers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/list-suppliers?${params}`, {
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
              "uploadedBy": "string",
              "uuid": "string"
            }
          ],
          "exportCode": "string",
          "favourite": true,
          "name": "Ava Chen",
          "notes": [
            {
              "createdAt": "string",
              "createdByUUID": "string",
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
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].addresses[].address` | string | The details of the address. |
| `data[].addresses[].city` | string | The city information of the address. |
| `data[].addresses[].country` | string | The country information of the address. |
| `data[].addresses[].postalCode` | string | The postal code information of the address. |
| `data[].addresses[].state` | string | The state information of the address. |
| `data[].addresses[].street` | string | The street information of the address. |
| `data[].addresses[].type` | string | The type of the address, e.g. physical or postal. |
| `data[].contactDetails.email` | string | The email address of the supplier. |
| `data[].contactDetails.fax` | string | The fax number of the supplier. |
| `data[].contactDetails.phone` | string | The phone number of the supplier. |
| `data[].contactDetails.website` | string | The website of the supplier. |
| `data[].contacts[].createdAt` | string | The date and time when the supplier contact was created. |
| `data[].contacts[].email` | string | The email address of the supplier contact. |
| `data[].contacts[].firstName` | string | The first name of the supplier contact. |
| `data[].contacts[].lastName` | string | The last name of the supplier contact. |
| `data[].contacts[].mobile` | string | The mobile number of the supplier contact. |
| `data[].contacts[].phone` | string | The phone number of the supplier contact. |
| `data[].contacts[].position` | string | The position of the supplier contact. |
| `data[].contacts[].updatedAt` | string | The date and time when the supplier contact was last updated. |
| `data[].contacts[].uuid` | string | The unique identifier of the supplier contact. |
| `data[].createdAt` | string | The UTC date and time when the supplier was created. |
| `data[].customFields[].name` | string | The name of the custom field. |
| `data[].customFields[].uuid` | string | The unique identifier of the custom field. |
| `data[].customFields[].value` | string | The value of the custom field. |
| `data[].deletedAt` | string | The UTC date and time when the supplier was deleted. It only populate when the supplier was deleted. |
| `data[].documents[].createdAt` | string | The UTC date and time when the document was created. |
| `data[].documents[].downloadURL` | string | The download URL of the document. |
| `data[].documents[].fileName` | string | The file name of the document. |
| `data[].documents[].fileSize` | number | The file size of the document. |
| `data[].documents[].note` | string | The note of the document. |
| `data[].documents[].phase` | string | The phase name of the document. |
| `data[].documents[].title` | string | The title of the document. |
| `data[].documents[].updatedAt` | string | The UTC date and time when the document was last updated. |
| `data[].documents[].uploadedBy` | string | The name of the staff who updated the document. |
| `data[].documents[].uuid` | string | The unique identifier of the document. |
| `data[].exportCode` | string | The export code of the supplier. |
| `data[].favourite` | boolean | Indicate whether the supplier is marked as favourite. |
| `data[].name` | string | The name of the supplier. |
| `data[].notes[].createdAt` | string | The UTC date and time when the note was created. |
| `data[].notes[].createdByUUID` | string | The unique identifier of the staff who created the note. |
| `data[].notes[].note` | string | The note details of the note. |
| `data[].notes[].phase` | string | The phase name of the note. |
| `data[].notes[].title` | string | The title of the note. |
| `data[].notes[].updatedAt` | string | The UTC date and time when the note was last updated. |
| `data[].notes[].uuid` | string | The unique identifier of the note. |
| `data[].status` | string | The status of the supplier, e.g. active, archived, deleted. |
| `data[].updatedAt` | string | The UTC date and time when the supplier was last updated. |
| `data[].uuid` | string | The unique identifier of the supplier. |
| `data[].zeroRatedGST[].rate` | number | The rate of the zero rated tax, it should always be 0. |
| `data[].zeroRatedGST[].tax_name` | string | The name of the zero rated tax. |
| `total` | number | The total number of suppliers returned. |

## Native endpoint

Through the native WorkflowMax API, this operation is `GET v2/suppliers` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-suppliers.md) for the provider-specific parameters and requirements.

