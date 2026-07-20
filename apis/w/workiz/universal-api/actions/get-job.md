# Workiz: Get Job

Retrieves a job from Workiz by UUID.

```
GET https://connect.mindcloud.co/v1/universal/workiz/latest/actions/get-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workiz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workiz/latest/actions/get-job?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workiz/latest/actions/get-job?${params}`, {
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
| `uuid` | string | yes | The job's UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "city": "string",
      "clientId": 1,
      "comments": "string",
      "company": "string",
      "country": "string",
      "createdDate": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "itemCost": 1,
      "jobAmountDue": 1,
      "jobDateTime": "string",
      "jobEndDateTime": "string",
      "jobNotes": "string",
      "jobSource": "string",
      "jobTotalPrice": 1,
      "jobType": "string",
      "lastName": "Chen",
      "lastStatusUpdate": "string",
      "latitude": 1,
      "lineItems": [
        "string"
      ],
      "locationId": 1,
      "locationKey": "string",
      "longitude": 1,
      "paymentDueDate": "string",
      "phone": "string",
      "phoneExt": "string",
      "postalCode": "string",
      "secondPhone": "string",
      "secondPhoneExt": "string",
      "serialId": 1,
      "state": "string",
      "status": "string",
      "subStatus": "string",
      "subTotal": 1,
      "tags": "string",
      "team": [
        "string"
      ],
      "techCost": 1,
      "unit": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `city` | string |  |
| `clientId` | number |  |
| `comments` | string |  |
| `company` | string |  |
| `country` | string |  |
| `createdDate` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `itemCost` | number |  |
| `jobAmountDue` | number |  |
| `jobDateTime` | string |  |
| `jobEndDateTime` | string |  |
| `jobNotes` | string |  |
| `jobSource` | string |  |
| `jobTotalPrice` | number |  |
| `jobType` | string |  |
| `lastName` | string |  |
| `lastStatusUpdate` | string |  |
| `latitude` | number |  |
| `lineItems` | array |  |
| `locationId` | number |  |
| `locationKey` | string |  |
| `longitude` | number |  |
| `paymentDueDate` | string |  |
| `phone` | string |  |
| `phoneExt` | string |  |
| `postalCode` | string |  |
| `secondPhone` | string |  |
| `secondPhoneExt` | string |  |
| `serialId` | number |  |
| `state` | string |  |
| `status` | string |  |
| `subStatus` | string |  |
| `subTotal` | number |  |
| `tags` | string |  |
| `team` | array |  |
| `techCost` | number |  |
| `unit` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Workiz API, this operation is `GET /job/get/:UUID/` (base URL `https://api.workiz.com/api/v1/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job.md) for the provider-specific parameters and requirements.

