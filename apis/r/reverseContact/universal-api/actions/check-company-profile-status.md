# Reverse Contact: Check Company Profile Status



```
GET https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/check-company-profile-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reverse Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/check-company-profile-status?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/check-company-profile-status?${params}`, {
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
| `url` | string | yes | Public Social company URL to check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "exists": true,
      "lastUpdate": "2026-05-07T12:00:00.000Z",
      "specialityCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `exists` | boolean |  |
| `lastUpdate` | date |  |
| `specialityCount` | number |  |

## Native endpoint

Through the native Reverse Contact API, this operation is `POST /v2/fetch/companies/check` (base URL `https://api.reversecontact.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-company-profile-status.md) for the provider-specific parameters and requirements.

