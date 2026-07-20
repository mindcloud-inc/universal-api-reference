# White Swan: List Personal Plans

Retrieves personal plans from White Swan.

```
GET https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/list-personal-plans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a White Swan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/list-personal-plans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/list-personal-plans?${params}`, {
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
| `planId` | string | no | Filter personal plans by White Swan plan ID. |
| `policySearch` | string | no | Filter personal plans by policy search ID. |
| `userEmail` | string | no | Filter personal plans by account user email. |
| `clientEmail` | string | no | Filter personal plans by client email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | object |  |
| `status` | string |  |

## Native endpoint

Through the native White Swan API, this operation is `POST /personal_plan` (base URL `https://app.whiteswan.io/api/1.1/wf`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-personal-plans.md) for the provider-specific parameters and requirements.

