# Postmaster+: Retrieve Domain

Retrieves domain details from the Postmaster+ API.

```
GET https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/retrieve-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmaster+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/retrieve-domain?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/retrieve-domain?${params}`, {
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
| `endDate` | string | no | Filter related IPs until this date (Y-m-d). Maximum selected range is 90 days. |
| `id` | string | yes | The ULID of the domain. |
| `relatedIpsPage` | number | no | The page number for related IP results. |
| `startDate` | string | no | Filter related IPs from this date (Y-m-d). Maximum selected range is 90 days. |

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
      "logo": "string",
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
| `compliance.isCompliant` | boolean | Whether the domain is compliant. |
| `createdAt` | string | Creation timestamp. |
| `description` | string | Domain description. |
| `id` | string | Domain ULID. |
| `logo` | string | Domain logo URL when available. |
| `team.name` | string | Owning team name. |
| `updatedAt` | string | Update timestamp. |
| `value` | string | Domain value. |

## Native endpoint

Through the native Postmaster+ API, this operation is `GET /api/v1/domains/:id` (base URL `https://postmasterplus.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-domain.md) for the provider-specific parameters and requirements.

