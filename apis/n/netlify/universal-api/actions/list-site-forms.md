# Netlify: List Site Forms



```
GET https://connect.mindcloud.co/v1/universal/netlify/latest/actions/list-site-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Netlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netlify/latest/actions/list-site-forms?connectionId=$CONNECTION_ID&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netlify/latest/actions/list-site-forms?${params}`, {
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
| `siteId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fields": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "paths": [
        "string"
      ],
      "siteId": "string",
      "submissionCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp |
| `fields` | array<object> | Form field definitions |
| `id` | string | Form ID |
| `name` | string | Form name |
| `paths` | array<string> | Paths where the form is embedded |
| `siteId` | string | Site ID |
| `submissionCount` | number | Number of submissions |

## Native endpoint

Through the native Netlify API, this operation is `GET /sites/:site_id/forms` (base URL `https://api.netlify.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-site-forms.md) for the provider-specific parameters and requirements.

