# Zoho FSM: Create Company

Creates a new company in Zoho FSM.

```
POST https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho FSM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data[0].Company_Name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoFSM/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data[0].Company_Name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data[0].Company_Name` | string | yes | The name of the company. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companies": [
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
          "tabName": "Ava Chen",
          "uid": "string"
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
| `companies[].createdBy.id` | string |  |
| `companies[].createdBy.name` | string |  |
| `companies[].createdTime` | date |  |
| `companies[].id` | string |  |
| `companies[].modifiedBy.id` | string |  |
| `companies[].modifiedBy.name` | string |  |
| `companies[].modifiedTime` | date |  |
| `companies[].tabName` | string |  |
| `companies[].uid` | string |  |

## Native endpoint

Through the native Zoho FSM API, this operation is `POST /Companies` (base URL `{{credentials.accessTokenRequest.api_domain}}/fsm/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.

