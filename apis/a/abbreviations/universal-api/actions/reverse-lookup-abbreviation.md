# Abbreviations: Reverse Lookup Abbreviation



```
GET https://connect.mindcloud.co/v1/universal/abbreviations/latest/actions/reverse-lookup-abbreviation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Abbreviations `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abbreviations/latest/actions/reverse-lookup-abbreviation?connectionId=$CONNECTION_ID&term=As%20Soon%20As%20Possible" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "term": "As Soon As Possible"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abbreviations/latest/actions/reverse-lookup-abbreviation?${params}`, {
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
| `term` | string | yes | The full term or phrase to reverse-search for abbreviation matches, such as `As Soon As Possible`. Example: `As Soon As Possible`. |
| `sortby` | list | no | Sort order: popularity, alphabetical, or category. One of: `a`, `c`, `p`. Default: `p`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `categoryid` | string | no | Optional STANDS4 category id to search within, such as `MEDICAL`. Example: `MEDICAL`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "categoryname": "Ava Chen",
      "definition": "string",
      "id": "string",
      "score": "string",
      "term": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | STANDS4 category code for this result. |
| `categoryname` | string | Display name for the result category. |
| `definition` | string | The definition found for the term. |
| `id` | string | STANDS4 result identifier. |
| `score` | string | STANDS4 relevance or rating score returned as a string. |
| `term` | string | The abbreviation or term for this result. |

## Native endpoint

Through the native Abbreviations API, this operation is `GET /abbr.php` (base URL `https://www.stands4.com/services/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reverse-lookup-abbreviation.md) for the provider-specific parameters and requirements.

