# FindyMail: Start Lead Search

Starts a lead search in FindyMail.

```
GET https://connect.mindcloud.co/v1/universal/findyMail/latest/actions/start-lead-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FindyMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/findyMail/latest/actions/start-lead-search?connectionId=$CONNECTION_ID&query=SaaS%20companies%20in%20US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "SaaS companies in US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/findyMail/latest/actions/start-lead-search?${params}`, {
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
| `query` | string | yes | Natural-language lead search query. Example: `SaaS companies in US`. |
| `limit` | number | no | Maximum number of lead results to request. Example: `100`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `config.findContact` | boolean | no | Whether FindyMail should find a contact for each matching company. Default: `true`. |
| `config.findEmail` | boolean | no | Whether FindyMail should find an email for each matching contact. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "contact_email": "ava@example.com",
          "domain": "string",
          "name": "Ava Chen"
        }
      ],
      "hash": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Lead search results returned when the API responds synchronously. |
| `data[].contact_email` | string | Email returned for the matching contact. |
| `data[].domain` | string | Matched company domain. |
| `data[].name` | string | Matched company name. |
| `hash` | string | Async search job hash returned by the Lead Finder API at runtime. |

## Native endpoint

Through the native FindyMail API, this operation is `POST /api/intellimatch/search` (base URL `https://app.findymail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-lead-search.md) for the provider-specific parameters and requirements.

