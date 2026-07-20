# Google Mail: Get Profile

Retrieves the current user's Gmail profile.

```
GET https://connect.mindcloud.co/v1/universal/gmail/latest/actions/get-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gmail/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gmail/latest/actions/get-profile?${params}`, {
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
| `alt` | string | no | default: 'json'. Media, and proto also available. Default: `json`. |
| `xgafv` | string | no | E(x)tended (G)oogle (A)PI (F)ormat (V)ersion. This is an error format version parameter. The parameter determines the format of error messages returned by the API. Options are (1) legacy error format or (2) the standard error format with enhanced error detail. Default: `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emailAddress": "ava@example.com",
      "historyId": "string",
      "messagesTotal": 1,
      "threadsTotal": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailAddress` | string |  |
| `historyId` | string |  |
| `messagesTotal` | number |  |
| `threadsTotal` | number |  |

## Native endpoint

Through the native Google Mail API, this operation is `GET /profile` (base URL `https://gmail.googleapis.com/gmail/v1/users/:userId`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-profile.md) for the provider-specific parameters and requirements.

