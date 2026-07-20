# WorkflowMax: Create Client



```
POST https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WorkflowMax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/create-client', {
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
          "businessStructure": "string",
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
          "numberOfShare": 1,
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
      "exportCode": "string",
      "favorite": true,
      "jobManager": {
        "firstName": "Ava",
        "lastName": "Chen",
        "uuid": "string"
      },
      "name": "Ava Chen",
      "prospect": true,
      "referralSource": "string",
      "updatedAt": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses[].address` | string | The full address. |
| `addresses[].city` | string | The city of the client address. |
| `addresses[].country` | string | The country where the client is located, typically represented by its ISO code. |
| `addresses[].default` | boolean | Indicate whether the address is a default one for the client. |
| `addresses[].postalCode` | string | The postal or ZIP code associated with the client’s address. |
| `addresses[].state` | string | The state, province, or region part of the client’s address. |
| `addresses[].type` | string | The classification or category of the address (e.g., billing, postal). |
| `archived` | boolean | Indicate whether the client is archived. |
| `billingDetails.balanceDate` | string | Client's balance date. |
| `billingDetails.billingClient.name` | string | The name of the billing client associated with the created client. |
| `billingDetails.billingClient.uuid` | string | The unique identifier of the billing client associated with the created client. |
| `billingDetails.businessStructure.businessStructure` | string | The name of the business structure. |
| `billingDetails.businessStructure.uuid` | string | The unique identifier of the business structure. |
| `billingDetails.clientType.clientType` | string | The name of the client type. |
| `billingDetails.clientType.uuid` | string | The unique identifier of the client type. |
| `billingDetails.customRates[].billableRate` | number | The custom billable rate of the task for the client. |
| `billingDetails.customRates[].taskUUID` | string | The unique identifier of the task having client custom rate. |
| `billingDetails.invoiceDueDate` | string | The payment term of the client. |
| `billingDetails.markup` | number | The percentage or fixed amount added to the client’s base rate as a markup. |
| `billingDetails.taxNumbers[].name` | string | The name of the tax. |
| `billingDetails.taxNumbers[].number` | string | Percentage rate of the tax. |
| `billingDetails.zeroRatedTaxRate.rate` | number | The percentage rate of the tax. It must be 0. |
| `billingDetails.zeroRatedTaxRate.taxName` | string | The name or description of the zero tax applied to the client’s transactions. |
| `clientGroups[].name` | string | The name of the client group. |
| `clientGroups[].taxable` | boolean | Indicate whether the client group is taxable. |
| `clientGroups[].uuid` | string | The unique identifier of the client group. |
| `clientManager.firstName` | string | The first name of the client manager. |
| `clientManager.lastName` | string | The last name of the client manager. |
| `clientManager.uuid` | string | The unique identifier of the client manager for the client. |
| `clientRelationships[].endDate` | string | The end date of the client relationship. |
| `clientRelationships[].numberOfShare` | number | Number of shares held by the client. It only has value in some specific relationships. |
| `clientRelationships[].relatedClientUUID` | string | The unique identifier of the client associated with the created client in the relationship. |
| `clientRelationships[].startDate` | string | The start date of the client relationship. |
| `clientRelationships[].type` | string | The type of the client relationship. |
| `clientRelationships[].uuid` | string | The unique identifier of the client relationship. |
| `contactDetails.email` | string | The primary email address associated with the client used for communication and notifications. |
| `contactDetails.fax` | string | The fax number assigned to the client for sending and receiving faxes. |
| `contactDetails.phone` | string | The primary telephone number for contacting the client. |
| `contactDetails.website` | string | The official website URL of the client’s business or organization. |
| `contacts[].firstName` | string | The first name of the client contact. |
| `contacts[].includeInEmails` | boolean | Indicate whether the contact should be included in the emails sent to the client. |
| `contacts[].lastName` | string | The last name of the client contact. |
| `contacts[].position` | string | The job title or role of the contact within the client’s organization. |
| `contacts[].primary` | boolean | Indicates whether this contact is marked as primary contact for the client's organization. |
| `contacts[].salutation` | string | The preferred salutation or title for the client (e.g., Mr., Ms., Dr.). |
| `contacts[].uuid` | string | The unique identifier of the client contact. |
| `createdAt` | string | The UTC timestamp indicating when the {object} was created. |
| `customFields[].name` | string | The name of the custom field. |
| `customFields[].uuid` | string | The unique identifier of the custom field. |
| `customFields[].value` | string | The value of the custom field. |
| `exportCode` | string | A code used to classify or manage the client for export or reporting purposes. |
| `favorite` | boolean | Indicate whether the client is marked as favorite. |
| `jobManager.firstName` | string | The first name of the job manager. |
| `jobManager.lastName` | string | The last name of the job manager. |
| `jobManager.uuid` | string | The unique identifier of the job manager for the client. |
| `name` | string | The full name of the client as a single string. |
| `prospect` | boolean | Indicate whether the client is a prospect. |
| `referralSource` | string | The origin or source through which the client was referred. |
| `updatedAt` | string | The UTC timestamp indicating when the {object} was last updated. |
| `uuid` | string | A unique identifier assigned to the client, typically in UUID format. |

## Native endpoint

Through the native WorkflowMax API, this operation is `POST v2/clients` (base URL `https://api.workflowmax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

