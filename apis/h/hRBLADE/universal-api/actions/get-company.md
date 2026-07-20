# HRBLADE: Get Company



```
GET https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HRBLADE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/get-company?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/get-company?${params}`, {
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
| `id` | number | yes | Company identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "error": true,
      "response": {
        "data": {
          "agencyId": 1,
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": 1,
          "logo": "string",
          "name": "Ava Chen",
          "permissions": {
            "createJobs": true,
            "createRooms": true,
            "editCompany": true,
            "viewJobs": true,
            "viewRooms": true
          },
          "shareHash": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `error` | boolean |  |
| `response.data.agencyId` | number |  |
| `response.data.createdAt` | date |  |
| `response.data.id` | number |  |
| `response.data.logo` | string |  |
| `response.data.name` | string |  |
| `response.data.permissions.createJobs` | boolean |  |
| `response.data.permissions.createRooms` | boolean |  |
| `response.data.permissions.editCompany` | boolean |  |
| `response.data.permissions.viewJobs` | boolean |  |
| `response.data.permissions.viewRooms` | boolean |  |
| `response.data.shareHash` | string |  |
| `response.data.updatedAt` | date |  |

## Native endpoint

Through the native HRBLADE API, this operation is `GET /company/get/:id` (base URL `https://api.hrblade.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

