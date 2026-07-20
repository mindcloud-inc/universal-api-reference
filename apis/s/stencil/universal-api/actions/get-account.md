# Stencil: Get Account



```
GET https://connect.mindcloud.co/v1/universal/stencil/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stencil `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stencil/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stencil/latest/actions/get-account?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currentProject": {},
      "currentUsage": 1,
      "email": "ava@example.com",
      "id": "string",
      "limitUsage": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the Stencil account was created. |
| `currentProject` | object | Current project scoped to the API key. |
| `currentUsage` | number | Current usage count for the account. |
| `email` | string | Email address for the Stencil account. |
| `id` | string | Stencil account identifier. |
| `limitUsage` | number | Usage limit for the current plan. |

## Native endpoint

Through the native Stencil API, this operation is `GET /v1/account` (base URL `https://api.usestencil.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

