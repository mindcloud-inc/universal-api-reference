# Seqera: List Organizations

Retrieves available organizations from Seqera.

```
GET https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seqera `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seqera/latest/actions/list-organizations?${params}`, {
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
      "organizations": [
        {
          "description": "string",
          "fullName": "Ava Chen",
          "location": "string",
          "logoId": "string",
          "logoUrl": "https://example.com",
          "memberId": 1,
          "memberRole": "string",
          "name": "Ava Chen",
          "orgId": 1,
          "paying": true,
          "type": "string",
          "website": "string"
        }
      ],
      "totalSize": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `organizations` | array<object> | Organizations available to the authenticated user. |
| `organizations[].description` | string | Organization description. |
| `organizations[].fullName` | string | Organization full name. |
| `organizations[].location` | string | Organization location. |
| `organizations[].logoId` | string | Organization logo ID. |
| `organizations[].logoUrl` | string | Organization logo URL. |
| `organizations[].memberId` | number | Membership ID for the authenticated user. |
| `organizations[].memberRole` | string | Role of the authenticated user in the organization. |
| `organizations[].name` | string | Organization short name. |
| `organizations[].orgId` | number | Organization ID. |
| `organizations[].paying` | boolean | Whether the organization is paying. |
| `organizations[].type` | string | Organization plan type. |
| `organizations[].website` | string | Organization website URL. |
| `totalSize` | number | Total number of organizations returned. |

## Native endpoint

Through the native Seqera API, this operation is `GET /orgs` (base URL `https://api.cloud.seqera.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

