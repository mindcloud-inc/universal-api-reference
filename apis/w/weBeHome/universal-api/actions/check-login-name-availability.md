# WeBeHome: Check Login Name Availability



```
GET https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/check-login-name-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeBeHome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/check-login-name-availability?connectionId=$CONNECTION_ID&LoginName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "LoginName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weBeHome/latest/actions/check-login-name-availability?${params}`, {
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
| `LoginName` | string | yes | Login name to check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Available": 1,
      "Created": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Available` | number |  |
| `Created` | string |  |

## Native endpoint

Through the native WeBeHome API, this operation is `POST OpenAPIservice.svc/CreateWebTokens/CheckLoginName` (base URL `https://webehome.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-login-name-availability.md) for the provider-specific parameters and requirements.

