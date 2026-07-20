# ContactOut: Search People

Finds people in ContactOut using people search filters.

```
GET https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/search-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContactOut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/search-people?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/search-people?${params}`, {
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
| `company` | string | no | Filter by current or past company. |
| `job_title` | string | no | Filter by job title. |
| `name` | string | no | Match people by name. |
| `page` | string | no | Results page number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "metadata": {
        "page": 1,
        "page_size": 1,
        "total_results": 1
      },
      "profiles": "string",
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
| `metadata.page` | number |  |
| `metadata.page_size` | number |  |
| `metadata.total_results` | number |  |
| `profiles` | string |  |
| `status_code` | number |  |

## Native endpoint

Through the native ContactOut API, this operation is `POST /v1/people/search` (base URL `https://api.contactout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-people.md) for the provider-specific parameters and requirements.

