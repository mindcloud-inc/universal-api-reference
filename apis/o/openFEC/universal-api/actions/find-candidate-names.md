# OpenFEC: Find Candidate Names

Finds candidate names in OpenFEC.

```
GET https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/find-candidate-names
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenFEC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/find-candidate-names?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openFEC/latest/actions/find-candidate-names?${params}`, {
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
| `q` | string | yes | Candidate name search text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "office_sought": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `office_sought` | string |  |

## Native endpoint

Through the native OpenFEC API, this operation is `GET /names/candidates/` (base URL `https://api.open.fec.gov/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-candidate-names.md) for the provider-specific parameters and requirements.

