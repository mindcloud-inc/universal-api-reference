# Bitly: Get Organization Plan Limits

Retrieves organization plan limits from Bitly.

```
GET https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-organization-plan-limits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-organization-plan-limits?connectionId=$CONNECTION_ID&organizationGuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationGuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-organization-plan-limits?${params}`, {
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
| `organizationGuid` | string | yes | The Bitly organization GUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "organizationGuid": "string",
      "planLimits": [
        {
          "count": 1,
          "description": "string",
          "limit": 1,
          "name": "Ava Chen"
        }
      ],
      "references": {
        "organization": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `organizationGuid` | string |  |
| `planLimits[].count` | number |  |
| `planLimits[].description` | string |  |
| `planLimits[].limit` | number |  |
| `planLimits[].name` | string |  |
| `references.organization` | string |  |

## Native endpoint

Through the native Bitly API, this operation is `GET /organizations/:organization_guid/plan_limits` (base URL `https://api-ssl.bitly.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-plan-limits.md) for the provider-specific parameters and requirements.

