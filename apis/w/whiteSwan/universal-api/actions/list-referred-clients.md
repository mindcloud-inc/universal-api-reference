# White Swan: List Referred Clients

Retrieves referred clients from White Swan.

```
GET https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/list-referred-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a White Swan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/list-referred-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whiteSwan/latest/actions/list-referred-clients?${params}`, {
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
| `clientEmail` | string | no | Optionally return one referred client by email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "associated_plan_ids": [
        "string"
      ],
      "associated_request_ids": [
        "string"
      ],
      "email": "ava@example.com",
      "name": "Ava Chen",
      "referrer": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `associated_plan_ids` | array<string> |  |
| `associated_request_ids` | array<string> |  |
| `email` | string |  |
| `name` | string |  |
| `referrer` | string |  |

## Native endpoint

Through the native White Swan API, this operation is `POST /client` (base URL `https://app.whiteswan.io/api/1.1/wf`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-referred-clients.md) for the provider-specific parameters and requirements.

