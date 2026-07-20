# Signaturit: Get Certified Email

Retrieves a certified email from Signaturit.

```
GET https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/get-certified-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Signaturit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/get-certified-email?connectionId=$CONNECTION_ID&id=bfc95b26-22f3-11f1-b406-066f594717e9" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "bfc95b26-22f3-11f1-b406-066f594717e9"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/get-certified-email?${params}`, {
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
| `id` | string | yes | Certified email identifier. Example: `bfc95b26-22f3-11f1-b406-066f594717e9`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "certificates": [
        {
          "created_at": "string",
          "email": "ava@example.com",
          "events": [
            {
              "created_at": "string",
              "type": "string"
            }
          ],
          "file": {
            "name": "Ava Chen",
            "size": 1
          },
          "id": "string",
          "name": "Ava Chen",
          "status": "string"
        }
      ],
      "created_at": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `certificates[].created_at` | string |  |
| `certificates[].email` | string |  |
| `certificates[].events[].created_at` | string |  |
| `certificates[].events[].type` | string |  |
| `certificates[].file.name` | string |  |
| `certificates[].file.size` | number |  |
| `certificates[].id` | string |  |
| `certificates[].name` | string |  |
| `certificates[].status` | string |  |
| `created_at` | string |  |
| `id` | string |  |

## Native endpoint

Through the native Signaturit API, this operation is `GET /emails/:id.json` (base URL `https://api.sandbox.signaturit.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-certified-email.md) for the provider-specific parameters and requirements.

