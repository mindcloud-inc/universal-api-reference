# Attio: Search Records

Finds records in Attio by fuzzy search.

```
GET https://connect.mindcloud.co/v1/universal/attio/latest/actions/search-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Attio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/attio/latest/actions/search-records?connectionId=$CONNECTION_ID&query=string&objects%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string",
  "objects[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/attio/latest/actions/search-records?${params}`, {
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
| `query` | string | yes | Query string to search for. An empty string returns a default set of results. |
| `objects[]` | array<string> | yes | One or more Attio object slugs or UUIDs to search within. |
| `limit` | number | no | Maximum number of results to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emailAddresses": [
        "ava@example.com"
      ],
      "id": {},
      "objectSlug": "string",
      "phoneNumbers": [
        "string"
      ],
      "recordImage": "string",
      "recordText": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailAddresses` | array<string> | Matched email addresses for the record. |
| `id` | object | Record identifier payload containing workspace, object, and record ids. |
| `objectSlug` | string | Object slug for the matched record. |
| `phoneNumbers` | array<string> | Matched phone numbers for the record. |
| `recordImage` | string | Record image URL when available. |
| `recordText` | string | Primary display text for the matched record. |

## Native endpoint

Through the native Attio API, this operation is `POST /v2/objects/records/search` (base URL `https://api.attio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-records.md) for the provider-specific parameters and requirements.

