# Rachio Smart Lighting Controller: Get Current Person Details



```
GET https://connect.mindcloud.co/v1/universal/rachioSmartLightingController/latest/actions/get-current-person-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rachio Smart Lighting Controller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rachioSmartLightingController/latest/actions/get-current-person-details?connectionId=$CONNECTION_ID&id=6c9ef499-10e7-40e4-9986-27aeb82a6d77" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "6c9ef499-10e7-40e4-9986-27aeb82a6d77"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rachioSmartLightingController/latest/actions/get-current-person-details?${params}`, {
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
| `id` | string | yes | The person ID returned by Get Current Person ID. Example: `6c9ef499-10e7-40e4-9986-27aeb82a6d77`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createDate": 1,
      "deleted": true,
      "devices": [
        {}
      ],
      "email": "ava@example.com",
      "fullName": "Ava Chen",
      "id": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createDate` | number |  |
| `deleted` | boolean |  |
| `devices` | array<object> |  |
| `email` | string |  |
| `fullName` | string |  |
| `id` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Rachio Smart Lighting Controller API, this operation is `GET https://api.rach.io/1/public/person/:id` (base URL `https://cloud-rest.rach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-person-details.md) for the provider-specific parameters and requirements.

