# Socie: Get Member



```
GET https://connect.mindcloud.co/v1/universal/socie/latest/actions/get-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socie/latest/actions/get-member?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socie/latest/actions/get-member?${params}`, {
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
| `identifier` | string | yes | The Socie id or externalId of the member. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "emailAddress": "ava@example.com",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the member was created in Socie. |
| `emailAddress` | string | The member email address. |
| `id` | string | The Socie member id. |

## Native endpoint

Through the native Socie API, this operation is `GET /api/v1/members/:identifier` (base URL `https://api.socie.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-member.md) for the provider-specific parameters and requirements.

