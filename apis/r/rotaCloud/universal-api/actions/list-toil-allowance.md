# RotaCloud: List Toil Allowance



```
GET https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-toil-allowance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-toil-allowance?connectionId=$CONNECTION_ID&year=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "year": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-toil-allowance?${params}`, {
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
| `year` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accrued_hours": 1,
      "has_toil_records": true,
      "remaining_hours": 1,
      "used_hours": 1,
      "user": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accrued_hours` | number |  |
| `has_toil_records` | boolean |  |
| `remaining_hours` | number |  |
| `used_hours` | number |  |
| `user` | number |  |

## Native endpoint

Through the native RotaCloud API, this operation is `GET /v1/toil_allowance/:year` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-toil-allowance.md) for the provider-specific parameters and requirements.

