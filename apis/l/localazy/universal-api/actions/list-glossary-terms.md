# Localazy: List Glossary Terms

Retrieves glossary terms from a Localazy project.

```
GET https://connect.mindcloud.co/v1/universal/localazy/latest/actions/list-glossary-terms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Localazy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/localazy/latest/actions/list-glossary-terms?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/localazy/latest/actions/list-glossary-terms?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "glossaries": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `glossaries` | array<object> | Glossary terms configured for the project. |

## Native endpoint

Through the native Localazy API, this operation is `GET /projects/:projectId/glossary` (base URL `https://api.localazy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-glossary-terms.md) for the provider-specific parameters and requirements.

