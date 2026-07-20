# Kintone: Get App Permissions

Retrieves app permissions from Kintone.

```
GET https://connect.mindcloud.co/v1/universal/kintone/latest/actions/get-app-permissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kintone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kintone/latest/actions/get-app-permissions?connectionId=$CONNECTION_ID&appId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kintone/latest/actions/get-app-permissions?${params}`, {
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
| `appId` | number | yes | The Kintone app ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "revision": "string",
      "rights": [
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
| `revision` | string |  |
| `rights` | array<object> |  |

## Native endpoint

Through the native Kintone API, this operation is `GET /app/acl.json` (base URL `{{credentials.baseUrl}}/k/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-app-permissions.md) for the provider-specific parameters and requirements.

