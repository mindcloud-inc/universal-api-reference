# Control D: List Custom Rules

Retrieves custom rules for a profile from Control D.

```
GET https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-custom-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Control D `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-custom-rules?connectionId=$CONNECTION_ID&profileId=string&folderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileId": "string",
  "folderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/controlD/latest/actions/list-custom-rules?${params}`, {
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
| `profileId` | string | yes | Primary key (PK) of the profile |
| `folderId` | string | yes | Folder ID (0 or omit for root) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": {},
      "group": 1,
      "order": 1,
      "PK": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | object |  |
| `group` | number |  |
| `order` | number |  |
| `PK` | string |  |

## Native endpoint

Through the native Control D API, this operation is `GET /profiles/:profileId/rules/:folderId` (base URL `https://api.controld.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-rules.md) for the provider-specific parameters and requirements.

