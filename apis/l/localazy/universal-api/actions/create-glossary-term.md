# Localazy: Create Glossary Term

Creates a new glossary term in a Localazy project.

```
POST https://connect.mindcloud.co/v1/universal/localazy/latest/actions/create-glossary-term
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Localazy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/localazy/latest/actions/create-glossary-term" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "term[]": [
    {}
  ],
  "term[].lang": "string",
  "term[].term": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/localazy/latest/actions/create-glossary-term', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "term[]": [{}],
    "term[].lang": "string",
    "term[].term": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Localazy project id or slug. |
| `description` | string | no | Glossary term description. |
| `translateTerm` | boolean | no | Whether Localazy should translate the term. |
| `caseSensitive` | boolean | no | Whether the term match is case-sensitive. |
| `exactMatch` | boolean | no | Whether Localazy should match the whole term exactly. |
| `term[]` | array<object> | yes | Source term plus translations. |
| `term[].lang` | string | yes | Language code for the glossary value. |
| `term[].term` | string | yes | Glossary value in the selected language. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string | Identifier of the created glossary term. |

## Native endpoint

Through the native Localazy API, this operation is `POST /projects/:projectId/glossary` (base URL `https://api.localazy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-glossary-term.md) for the provider-specific parameters and requirements.

