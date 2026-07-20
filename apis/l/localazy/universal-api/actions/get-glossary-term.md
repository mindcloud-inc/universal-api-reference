# Localazy: Get Glossary Term

Retrieves a glossary term from a Localazy project.

```
GET https://connect.mindcloud.co/v1/universal/localazy/latest/actions/get-glossary-term
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Localazy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/localazy/latest/actions/get-glossary-term?connectionId=$CONNECTION_ID&projectId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/localazy/latest/actions/get-glossary-term?${params}`, {
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
| `projectId` | string | yes | Localazy project id or slug. |
| `id` | string | yes | Glossary term identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "caseSensitive": true,
      "description": "string",
      "exactMatch": true,
      "id": "string",
      "term": [
        {}
      ],
      "translateTerm": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `caseSensitive` | boolean | Whether matching is case-sensitive. |
| `description` | string | Optional glossary description. |
| `exactMatch` | boolean | Whether only exact matches should trigger the glossary entry. |
| `id` | string | Unique glossary term identifier. |
| `term` | array<object> | Localized term variants keyed by language. |
| `translateTerm` | boolean | Whether Localazy may translate the term automatically. |

## Native endpoint

Through the native Localazy API, this operation is `GET /projects/:projectId/glossary/:id` (base URL `https://api.localazy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-glossary-term.md) for the provider-specific parameters and requirements.

