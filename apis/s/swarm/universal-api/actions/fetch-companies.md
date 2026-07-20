# Swarm: Fetch Companies

Retrieves companies from Swarm by company ID.

```
GET https://connect.mindcloud.co/v1/universal/swarm/latest/actions/fetch-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swarm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swarm/latest/actions/fetch-companies?connectionId=$CONNECTION_ID&ids%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swarm/latest/actions/fetch-companies?${params}`, {
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
| `fields[]` | array<string> | no | Optional response fields such as company_info or tags. Provide a JSON array when needed. Accepts multiple values as an array. |
| `ids[]` | array<string> | yes | One or more Swarm company IDs to fetch. Provide a JSON array of IDs or add values in the UI. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
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
| `results` | array<object> | Fetched company records keyed by requested fields. |

## Native endpoint

Through the native Swarm API, this operation is `POST /companies/fetch` (base URL `https://bee.theswarm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-companies.md) for the provider-specific parameters and requirements.

