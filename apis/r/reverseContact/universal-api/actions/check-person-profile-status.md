# Reverse Contact: Check Person Profile Status



```
GET https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/check-person-profile-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reverse Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/check-person-profile-status?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/check-person-profile-status?${params}`, {
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
| `url` | string | yes | Public Social profile URL to check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "exists": true,
      "experienceCount": 1,
      "lastUpdate": "2026-05-07T12:00:00.000Z",
      "schoolCount": 1,
      "skillCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `exists` | boolean |  |
| `experienceCount` | number |  |
| `lastUpdate` | date |  |
| `schoolCount` | number |  |
| `skillCount` | number |  |

## Native endpoint

Through the native Reverse Contact API, this operation is `POST /v2/fetch/persons/check` (base URL `https://api.reversecontact.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-person-profile-status.md) for the provider-specific parameters and requirements.

