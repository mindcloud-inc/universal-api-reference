# Gupshup: Get Business Profile Details

Retrieves business profile details from Gupshup.

```
GET https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/get-business-profile-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gupshup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/get-business-profile-details?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gupshup/latest/actions/get-business-profile-details?${params}`, {
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
| `appId` | string | yes | Gupshup app ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "description": "string",
      "email": "ava@example.com",
      "websites": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object | Business address details. |
| `description` | string | Business profile description. |
| `email` | string | Business email address. |
| `websites` | array<string> | Business website URLs. |

## Native endpoint

Through the native Gupshup API, this operation is `GET /wa/app/{appId}/business/profile` (base URL `https://api.gupshup.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-business-profile-details.md) for the provider-specific parameters and requirements.

