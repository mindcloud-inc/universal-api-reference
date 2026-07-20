# KleverKey: Get Invitation



```
GET https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/get-invitation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KleverKey `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/get-invitation?connectionId=$CONNECTION_ID&organizationId=1&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "1",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kleverKey/latest/actions/get-invitation?${params}`, {
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
| `organizationId` | number | yes |  |
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateUpdated": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "organization": {},
      "receiverEmail": "ava@example.com",
      "status": 1,
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `dateCreated` | date |  |
| `dateUpdated` | date |  |
| `id` | number |  |
| `organization` | object |  |
| `receiverEmail` | string |  |
| `status` | number |  |
| `type` | number |  |

## Native endpoint

Through the native KleverKey API, this operation is `GET /api/v1/organizations/:organizationId/invitations/:id` (base URL `https://api.kleverkey.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invitation.md) for the provider-specific parameters and requirements.

