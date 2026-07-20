# Rosette Text Analytics: Compare Name Similarity



```
GET https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/compare-name-similarity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rosette Text Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/compare-name-similarity?connectionId=$CONNECTION_ID&name1.text=Ava%20Chen&name2.text=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name1.text": "Ava Chen",
  "name2.text": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rosetteTextAnalytics/latest/actions/compare-name-similarity?${params}`, {
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
| `name1.text` | string | yes | First name text to compare. |
| `name1.language` | string | no | Three-letter ISO 639-3 language code for the first name. |
| `name1.entityType` | string | no | Entity type such as PERSON, LOCATION, ORGANIZATION, or IDENTIFIER. Default: `PERSON`. |
| `name2.text` | string | yes | Second name text to compare. |
| `name2.language` | string | no | Three-letter ISO 639-3 language code for the second name. |
| `name2.entityType` | string | no | Entity type such as PERSON, LOCATION, ORGANIZATION, or IDENTIFIER. Default: `PERSON`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "score": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `score` | number |  |

## Native endpoint

Through the native Rosette Text Analytics API, this operation is `POST /name-similarity` (base URL `https://api.rosette.com/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compare-name-similarity.md) for the provider-specific parameters and requirements.

