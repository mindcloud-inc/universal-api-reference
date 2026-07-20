# Umbler Talk: Get Organization

Retrieves an organization summary from Umbler Talk.

```
GET https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbler Talk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/get-organization?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/get-organization?${params}`, {
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
| `id` | string | yes | The organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_t": "string",
      "channels": [
        {}
      ],
      "contractStatus": "string",
      "createdAtUTC": "2026-05-07T12:00:00.000Z",
      "features": {},
      "hasSentFirstMessage": true,
      "id": "string",
      "maxMembers": 1,
      "name": "Ava Chen",
      "organizationMembers": [
        {}
      ],
      "sectors": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_t` | string |  |
| `channels` | array<object> |  |
| `contractStatus` | string |  |
| `createdAtUTC` | date |  |
| `features` | object |  |
| `hasSentFirstMessage` | boolean |  |
| `id` | string |  |
| `maxMembers` | number |  |
| `name` | string |  |
| `organizationMembers` | array<object> |  |
| `sectors` | array<object> |  |

## Native endpoint

Through the native Umbler Talk API, this operation is `GET /v1/organizations/[:id]/` (base URL `https://app-utalk.umbler.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

