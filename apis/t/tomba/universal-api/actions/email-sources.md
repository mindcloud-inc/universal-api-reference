# Tomba: Email Sources

Retrieves email sources from Tomba.

```
GET https://connect.mindcloud.co/v1/universal/tomba/latest/actions/email-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tomba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tomba/latest/actions/email-sources?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tomba/latest/actions/email-sources?${params}`, {
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
| `email` | string | yes | Email address to retrieve source evidence for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "extracted_on": "2026-05-07T12:00:00.000Z",
          "last_seen_on": "2026-05-07T12:00:00.000Z",
          "still_on_page": true,
          "uri": "string",
          "website_url": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[].extracted_on` | date |  |
| `[].last_seen_on` | date |  |
| `[].still_on_page` | boolean |  |
| `[].uri` | string |  |
| `[].website_url` | string |  |

## Native endpoint

Through the native Tomba API, this operation is `GET /email-sources` (base URL `https://api.tomba.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/email-sources.md) for the provider-specific parameters and requirements.

