# ContactOut: Check Phone Status

Retrieves phone availability for a LinkedIn profile in ContactOut.

```
GET https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/check-phone-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContactOut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/check-phone-status?connectionId=$CONNECTION_ID&profile=https%3A%2F%2Fwww.linkedin.com%2Fin%2Fexample-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profile": "https://www.linkedin.com/in/example-person"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/check-phone-status?${params}`, {
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
| `profile` | string | yes | The full LinkedIn profile URL. Must begin with http and contain linkedin.com/in/ or linkedin.com/pub/. Example: `https://www.linkedin.com/in/example-person`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "profile": {
        "phone": true
      },
      "status_code": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `profile.phone` | boolean |  |
| `status_code` | number |  |

## Native endpoint

Through the native ContactOut API, this operation is `GET /v1/people/linkedin/phone_status` (base URL `https://api.contactout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-phone-status.md) for the provider-specific parameters and requirements.

