# Zoho FSM: List Requests

Retrieves requests from Zoho FSM.

```
GET https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/list-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho FSM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/list-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/list-requests?${params}`, {
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
      "billingAddress": {
        "billingCity": "string",
        "billingCountry": "string",
        "billingState": "string",
        "billingStreet1": "string",
        "billingZipCode": "string",
        "id": "string",
        "name": "Ava Chen"
      },
      "cancelledOrTerminatedTime": "2026-05-07T12:00:00.000Z",
      "closedTime": "2026-05-07T12:00:00.000Z",
      "company": {
        "id": "string",
        "name": "Ava Chen"
      },
      "completedTime": "2026-05-07T12:00:00.000Z",
      "contact": {
        "id": "string",
        "name": "Ava Chen"
      },
      "createdBy": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "createdTime": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "estimateRequired": true,
      "exchangeRate": 1,
      "id": "string",
      "modifiedBy": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "owner": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "phone": "string",
      "serviceAddress": {
        "id": "string",
        "name": "Ava Chen",
        "serviceCity": "string",
        "serviceCountry": "string",
        "serviceState": "string",
        "serviceStreet1": "string",
        "serviceZipCode": "string"
      },
      "status": "string",
      "summary": "string",
      "territory": {
        "id": "string",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingAddress.billingCity` | string |  |
| `billingAddress.billingCountry` | string |  |
| `billingAddress.billingState` | string |  |
| `billingAddress.billingStreet1` | string |  |
| `billingAddress.billingZipCode` | string |  |
| `billingAddress.id` | string |  |
| `billingAddress.name` | string |  |
| `cancelledOrTerminatedTime` | date |  |
| `closedTime` | date |  |
| `company.id` | string |  |
| `company.name` | string |  |
| `completedTime` | date |  |
| `contact.id` | string |  |
| `contact.name` | string |  |
| `createdBy.email` | string |  |
| `createdBy.id` | string |  |
| `createdBy.name` | string |  |
| `createdTime` | date |  |
| `currency` | string |  |
| `dueDate` | date |  |
| `email` | string |  |
| `estimateRequired` | boolean |  |
| `exchangeRate` | number |  |
| `id` | string |  |
| `modifiedBy.email` | string |  |
| `modifiedBy.id` | string |  |
| `modifiedBy.name` | string |  |
| `modifiedTime` | date |  |
| `name` | string |  |
| `owner.email` | string |  |
| `owner.id` | string |  |
| `owner.name` | string |  |
| `phone` | string |  |
| `serviceAddress.id` | string |  |
| `serviceAddress.name` | string |  |
| `serviceAddress.serviceCity` | string |  |
| `serviceAddress.serviceCountry` | string |  |
| `serviceAddress.serviceState` | string |  |
| `serviceAddress.serviceStreet1` | string |  |
| `serviceAddress.serviceZipCode` | string |  |
| `status` | string |  |
| `summary` | string |  |
| `territory.id` | string |  |
| `territory.name` | string |  |

## Native endpoint

Through the native Zoho FSM API, this operation is `GET /Requests` (base URL `{{credentials.accessTokenRequest.api_domain}}/fsm/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-requests.md) for the provider-specific parameters and requirements.

