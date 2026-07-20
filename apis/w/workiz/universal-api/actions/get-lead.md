# Workiz: Get Lead

Retrieves a lead from Workiz by UUID.

```
GET https://connect.mindcloud.co/v1/universal/workiz/latest/actions/get-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workiz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workiz/latest/actions/get-lead?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workiz/latest/actions/get-lead?${params}`, {
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
| `uuid` | string | yes | The lead's UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "city": "string",
      "clientId": "string",
      "comments": "string",
      "company": "string",
      "country": "string",
      "createdBy": "string",
      "createdDate": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "jobSource": "string",
      "lastName": "Chen",
      "lastStatusUpdate": "string",
      "latitude": "string",
      "leadDateTime": "string",
      "leadEndDateTime": "string",
      "leadNotes": "string",
      "lineItems": [
        {}
      ],
      "longitude": "string",
      "paymentDueDate": "string",
      "phone": "string",
      "phoneExt": "string",
      "postalCode": "string",
      "secondPhone": "string",
      "secondPhoneExt": "string",
      "serialId": "string",
      "state": "string",
      "status": "string",
      "subStatus": "string",
      "tags": "string",
      "team": [
        {}
      ],
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
| `clientId` | string |  |
| `comments` | string |  |
| `company` | string |  |
| `country` | string |  |
| `createdBy` | string |  |
| `createdDate` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `jobSource` | string |  |
| `lastName` | string |  |
| `lastStatusUpdate` | string |  |
| `latitude` | string |  |
| `leadDateTime` | string |  |
| `leadEndDateTime` | string |  |
| `leadNotes` | string |  |
| `lineItems` | array<object> |  |
| `longitude` | string |  |
| `paymentDueDate` | string |  |
| `phone` | string |  |
| `phoneExt` | string |  |
| `postalCode` | string |  |
| `secondPhone` | string |  |
| `secondPhoneExt` | string |  |
| `serialId` | string |  |
| `state` | string |  |
| `status` | string |  |
| `subStatus` | string |  |
| `tags` | string |  |
| `team` | array<object> |  |
| `unit` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Workiz API, this operation is `GET /lead/get/:UUID/` (base URL `https://api.workiz.com/api/v1/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead.md) for the provider-specific parameters and requirements.

