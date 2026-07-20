# Pappers: Get Latest Statutes



```
GET https://connect.mindcloud.co/v1/universal/pappers/latest/actions/get-latest-statutes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pappers `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pappers/latest/actions/get-latest-statutes?connectionId=$CONNECTION_ID&siren=542065479" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "siren": "542065479"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pappers/latest/actions/get-latest-statutes?${params}`, {
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
| `siren` | string | yes | Company SIREN number. Example: `542065479`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Pappers API, this operation is `GET /document/statuts` (base URL `https://api.pappers.fr/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-latest-statutes.md) for the provider-specific parameters and requirements.

