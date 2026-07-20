# RotaCloud: Get Toil Accrual

Retrieves a toil accrual record from RotaCloud.

```
GET https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-toil-accrual
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-toil-accrual?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-toil-accrual?${params}`, {
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
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": "string",
      "date": "string",
      "deleted": true,
      "duration_hours": 1,
      "id": 1,
      "leave_year": 1,
      "location_id": 1,
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | string |  |
| `date` | string |  |
| `deleted` | boolean |  |
| `duration_hours` | number |  |
| `id` | number |  |
| `leave_year` | number |  |
| `location_id` | number |  |
| `user_id` | number |  |

## Native endpoint

Through the native RotaCloud API, this operation is `GET /v1/toil_accruals/:id` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-toil-accrual.md) for the provider-specific parameters and requirements.

