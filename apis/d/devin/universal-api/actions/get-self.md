# Devin: Get Self

Retrieves the authenticated user from Devin.

```
GET https://connect.mindcloud.co/v1/universal/devin/latest/actions/get-self
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Devin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devin/latest/actions/get-self?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devin/latest/actions/get-self?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "org_id": "string",
      "principal_type": "string",
      "service_user_id": "string",
      "service_user_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `org_id` | string | Organization ID associated with the principal. |
| `principal_type` | string | Authenticated principal type. |
| `service_user_id` | string | Authenticated Devin service user ID. |
| `service_user_name` | string | Authenticated Devin service user name. |

## Native endpoint

Through the native Devin API, this operation is `GET /v3/self` (base URL `https://api.devin.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-self.md) for the provider-specific parameters and requirements.

