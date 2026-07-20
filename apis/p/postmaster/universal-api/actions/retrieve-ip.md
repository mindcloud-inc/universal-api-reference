# Postmaster+: Retrieve IP

Retrieves IP details from the Postmaster+ API.

```
GET https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/retrieve-ip
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmaster+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/retrieve-ip?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/retrieve-ip?${params}`, {
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
| `endDate` | string | no | Filter related domains until this date (Y-m-d). Maximum selected range is 90 days. |
| `id` | string | yes | The ULID of the IP. |
| `relatedDomainsPage` | number | no | The page number for related domain results. |
| `startDate` | string | no | Filter related domains from this date (Y-m-d). Maximum selected range is 90 days. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "compliance": {
        "isCompliant": true
      },
      "createdAt": "string",
      "description": "string",
      "id": "string",
      "team": {
        "name": "Ava Chen"
      },
      "updatedAt": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `compliance.isCompliant` | boolean | Whether the IP is compliant. |
| `createdAt` | string | Creation timestamp. |
| `description` | string | IP description. |
| `id` | string | IP ULID. |
| `team.name` | string | Owning team name. |
| `updatedAt` | string | Update timestamp. |
| `value` | string | IP value. |

## Native endpoint

Through the native Postmaster+ API, this operation is `GET /api/v1/ips/:id` (base URL `https://postmasterplus.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-ip.md) for the provider-specific parameters and requirements.

