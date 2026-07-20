# GoDial: Get Contact List

Retrieves a contact list from GoDial.

```
GET https://connect.mindcloud.co/v1/universal/goDial/latest/actions/lists-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDial `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goDial/latest/actions/lists-view?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goDial/latest/actions/lists-view?${params}`, {
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
| `id` | string | yes | List ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accounts": [
        {}
      ],
      "callScript": "string",
      "companyId": "string",
      "id": "string",
      "indiamart": {},
      "name": "Ava Chen",
      "system": true,
      "teamsId": "string",
      "twillioAudioUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accounts` | array<object> |  |
| `callScript` | string |  |
| `companyId` | string |  |
| `id` | string |  |
| `indiamart` | object |  |
| `name` | string |  |
| `system` | boolean |  |
| `teamsId` | string |  |
| `twillioAudioUrl` | string |  |

## Native endpoint

Through the native GoDial API, this operation is `GET /externals/lists/[:id]/view` (base URL `https://enterprise.godial.cc/meta/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lists-view.md) for the provider-specific parameters and requirements.

