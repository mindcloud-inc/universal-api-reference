# Jotform: Get User Setting By Key

Retrieves a user setting from Jotform.

```
GET https://connect.mindcloud.co/v1/universal/jotform/latest/actions/get-user-setting-by-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jotform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jotform/latest/actions/get-user-setting-by-key?connectionId=$CONNECTION_ID&settingsKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "settingsKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jotform/latest/actions/get-user-setting-by-key?${params}`, {
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
| `settingsKey` | string | yes | Settings key |

## Response

```json
{
  "success": true,
  "data": [
    {
      "language": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `language` | string |  |

## Native endpoint

Through the native Jotform API, this operation is `GET /user/settings/:settingsKey` (base URL `https://api.jotform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-setting-by-key.md) for the provider-specific parameters and requirements.

