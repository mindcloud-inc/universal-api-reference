# Clearout: Reverse Lookup LinkedIn Profile

Retrieves lead information from Clearout by LinkedIn profile URL.

```
GET https://connect.mindcloud.co/v1/universal/clearout/latest/actions/reverse-lookup-linked-in-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clearout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clearout/latest/actions/reverse-lookup-linked-in-profile?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clearout/latest/actions/reverse-lookup-linked-in-profile?${params}`, {
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
| `url` | string | yes | LinkedIn profile URL to lookup |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lead": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lead` | object |  |

## Native endpoint

Through the native Clearout API, this operation is `GET /reverse_lookup/linkedin` (base URL `https://api.clearout.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reverse-lookup-linked-in-profile.md) for the provider-specific parameters and requirements.

