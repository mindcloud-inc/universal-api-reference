# Signaturit: Get Signature

Retrieves a signature from Signaturit.

```
GET https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/get-signature
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Signaturit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/get-signature?connectionId=$CONNECTION_ID&id=389850f6-88fc-4cdc-8318-da4f5b538a19" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "389850f6-88fc-4cdc-8318-da4f5b538a19"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/get-signature?${params}`, {
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
| `id` | string | yes | Signature request identifier. Example: `389850f6-88fc-4cdc-8318-da4f5b538a19`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "documents": [
        {
          "created_at": "string",
          "email": "ava@example.com",
          "events": [
            {
              "created_at": "string",
              "reason": "string",
              "type": "string"
            }
          ],
          "file": {
            "name": "Ava Chen",
            "pages": 1,
            "size": 1
          },
          "id": "string",
          "name": "Ava Chen",
          "status": "string"
        }
      ],
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `documents[].created_at` | string |  |
| `documents[].email` | string |  |
| `documents[].events[].created_at` | string |  |
| `documents[].events[].reason` | string |  |
| `documents[].events[].type` | string |  |
| `documents[].file.name` | string |  |
| `documents[].file.pages` | number |  |
| `documents[].file.size` | number |  |
| `documents[].id` | string |  |
| `documents[].name` | string |  |
| `documents[].status` | string |  |
| `id` | string |  |

## Native endpoint

Through the native Signaturit API, this operation is `GET /signatures/:id.json` (base URL `https://api.sandbox.signaturit.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signature.md) for the provider-specific parameters and requirements.

