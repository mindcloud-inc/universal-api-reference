# Zoho FSM: Create Request

Creates a new request in Zoho FSM.

```
POST https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/create-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho FSM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/create-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data[].summary": "string",
  "data[].contact": "string",
  "data[].company": "string",
  "data[].serviceAddress": {},
  "data[].billingAddress": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/create-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data[].summary": "string",
    "data[].contact": "string",
    "data[].company": "string",
    "data[].serviceAddress": {},
    "data[].billingAddress": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data[].summary` | string | yes |  |
| `data[].contact` | string | yes |  |
| `data[].company` | string | yes |  |
| `data[].serviceAddress` | object | yes | The service address for the request. |
| `data[].billingAddress` | object | yes | The billing address for the request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "data": {
        "requests": [
          {
            "createdBy": {
              "id": "string",
              "name": "Ava Chen"
            },
            "createdTime": "2026-05-07T12:00:00.000Z",
            "id": "string",
            "modifiedBy": {
              "id": "string",
              "name": "Ava Chen"
            },
            "modifiedTime": "2026-05-07T12:00:00.000Z",
            "tabName": "Ava Chen"
          }
        ]
      },
      "details": {
        "createdBy": {
          "id": "string",
          "name": "Ava Chen"
        },
        "createdTime": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "modifiedBy": {
          "id": "string",
          "name": "Ava Chen"
        },
        "modifiedTime": "2026-05-07T12:00:00.000Z"
      },
      "message": "string",
      "result": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `data.requests[].createdBy.id` | string |  |
| `data.requests[].createdBy.name` | string |  |
| `data.requests[].createdTime` | date |  |
| `data.requests[].id` | string |  |
| `data.requests[].modifiedBy.id` | string |  |
| `data.requests[].modifiedBy.name` | string |  |
| `data.requests[].modifiedTime` | date |  |
| `data.requests[].tabName` | string |  |
| `details.createdBy.id` | string |  |
| `details.createdBy.name` | string |  |
| `details.createdTime` | date |  |
| `details.id` | string |  |
| `details.modifiedBy.id` | string |  |
| `details.modifiedBy.name` | string |  |
| `details.modifiedTime` | date |  |
| `message` | string |  |
| `result` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho FSM API, this operation is `POST /Requests` (base URL `{{credentials.accessTokenRequest.api_domain}}/fsm/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-request.md) for the provider-specific parameters and requirements.

