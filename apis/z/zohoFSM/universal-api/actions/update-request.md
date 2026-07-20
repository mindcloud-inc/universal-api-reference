# Zoho FSM: Update Request

Updates an existing request in Zoho FSM.

```
PUT https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/update-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho FSM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/update-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data[].summary": "string",
  "recordId": "string",
  "data[].contact": "string",
  "data[].company": "string",
  "data[].serviceAddress": {},
  "data[].billingAddress": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/update-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data[].summary": "string",
    "recordId": "string",
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
| `recordId` | string | yes | The Zoho FSM record ID. |
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
| `details.createdBy.id` | string |  |
| `details.createdBy.name` | string |  |
| `details.createdTime` | date |  |
| `details.id` | string |  |
| `details.modifiedBy.id` | string |  |
| `details.modifiedBy.name` | string |  |
| `details.modifiedTime` | date |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho FSM API, this operation is `PUT /Requests/:recordId` (base URL `{{credentials.accessTokenRequest.api_domain}}/fsm/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-request.md) for the provider-specific parameters and requirements.

