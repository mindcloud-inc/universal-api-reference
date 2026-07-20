# ManyReach: List Clientspaces

Retrieves clientspaces from ManyReach.

```
GET https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-clientspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-clientspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/list-clientspaces?${params}`, {
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
      "apiKey": "string",
      "autoAllocate": true,
      "clientspaceId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creditAmount": 1,
      "separateCredits": true,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiKey` | string | API key for authenticating requests made on behalf of this clientspace, represented as a GUID. |
| `autoAllocate` | boolean | Enables automatic recurring credit allocation to the clientspace, useful for subscription-based credit provisioning. |
| `clientspaceId` | number | Unique identifier for the clientspace (whitelabel sub-organization) within the agency. |
| `createdAt` | date | Timestamp when the clientspace was created in the system. |
| `creditAmount` | number | The number of credits to allocate when auto-allocation is enabled, defining the recurring credit amount for this clientspace. |
| `separateCredits` | boolean | Indicates whether the clientspace has a separate credit pool independent from the parent agency, allowing dedicated credit allocation for this client. |
| `title` | string | Display name of the clientspace; maximum 256 characters. |

## Native endpoint

Through the native ManyReach API, this operation is `GET https://api.manyreach.com/api/v2/clientspaces` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-clientspaces.md) for the provider-specific parameters and requirements.

