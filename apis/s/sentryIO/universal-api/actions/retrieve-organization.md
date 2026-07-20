# Sentry IO: Retrieve Organization

Retrieves an organization from Sentry IO.

```
GET https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/retrieve-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sentry IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/retrieve-organization?connectionId=$CONNECTION_ID&organizationIdOrSlug=my-org" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationIdOrSlug": "my-org"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/retrieve-organization?${params}`, {
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
| `organizationIdOrSlug` | string | yes | The Sentry organization ID or slug. Example: `my-org`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "slug": "string",
      "status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreated` | date | Organization creation timestamp. |
| `id` | string | Organization identifier. |
| `name` | string | Organization name. |
| `slug` | string | Organization slug. |
| `status` | object | Organization status object. |

## Native endpoint

Through the native Sentry IO API, this operation is `GET /organizations/:organization_id_or_slug/` (base URL `https://sentry.io/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-organization.md) for the provider-specific parameters and requirements.

