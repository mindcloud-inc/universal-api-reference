# Wiza: Get Individual Reveal

Retrieves an individual reveal from Wiza.

```
GET https://connect.mindcloud.co/v1/universal/wiza/latest/actions/get-individual-reveal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wiza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wiza/latest/actions/get-individual-reveal?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wiza/latest/actions/get-individual-reveal?${params}`, {
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
| `id` | number | yes | ID of the reveal to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "company": "string",
        "email": "ava@example.com",
        "id": 1,
        "is_complete": true,
        "mobile_phone": "string",
        "name": "Ava Chen",
        "status": "string"
      },
      "status": {
        "code": 1,
        "message": "string"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.company` | string | Company name. |
| `data.email` | string | Primary revealed email. |
| `data.id` | number | Reveal ID. |
| `data.is_complete` | boolean | Whether the reveal has completed. |
| `data.mobile_phone` | string | Primary revealed mobile phone. |
| `data.name` | string | Person name. |
| `data.status` | string | Current reveal status. |
| `status.code` | number | HTTP-style status code returned by Wiza. |
| `status.message` | string | Status message from Wiza. |
| `type` | string | Response type identifier. |

## Native endpoint

Through the native Wiza API, this operation is `GET /individual_reveals/:id` (base URL `https://wiza.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-individual-reveal.md) for the provider-specific parameters and requirements.

