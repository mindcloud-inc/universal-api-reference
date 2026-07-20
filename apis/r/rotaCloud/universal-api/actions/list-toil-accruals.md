# RotaCloud: List Toil Accruals

Lists toil accruals in RotaCloud.

```
GET https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-toil-accruals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-toil-accruals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-toil-accruals?${params}`, {
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
| `users` | number | no | Accepts multiple values in one string, delimited by `,`. |
| `year` | number | no |  |

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

Through the native RotaCloud API, this operation is `GET /v1/toil_accruals` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-toil-accruals.md) for the provider-specific parameters and requirements.

