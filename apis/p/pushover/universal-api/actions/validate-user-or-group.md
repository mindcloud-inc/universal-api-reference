# Pushover: Validate User or Group



```
GET https://connect.mindcloud.co/v1/universal/pushover/latest/actions/validate-user-or-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushover `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushover/latest/actions/validate-user-or-group?connectionId=$CONNECTION_ID&user=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "user": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushover/latest/actions/validate-user-or-group?${params}`, {
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
| `user` | string | yes | User key or group key to validate. |
| `device` | string | no | Optional device name to validate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "devices": [
        "string"
      ],
      "group": 1,
      "licenses": [
        "string"
      ],
      "request": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `devices` | array<string> | Active device names for the validated user. |
| `group` | number | Indicates whether the validated key is a group key. |
| `licenses` | array<string> | Licensed platforms for the validated account. |
| `request` | string | Pushover request identifier. |
| `status` | number | Validation status. Returns 1 for a valid target and 0 otherwise. |

## Native endpoint

Through the native Pushover API, this operation is `POST /users/validate.json` (base URL `https://api.pushover.net/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-user-or-group.md) for the provider-specific parameters and requirements.

