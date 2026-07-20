# Universe: List Stripe Countries

Retrieves available Stripe countries from Universe.

```
GET https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-stripe-countries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Universe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-stripe-countries?connectionId=$CONNECTION_ID&query=query%20ListStripeCountries%20%7B%0A%20%20availableStripeCountries%20%7B%0A%20%20%20%20code%0A%20%20%20%20country%0A%20%20%7D%0A%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query ListStripeCountries {\n  availableStripeCountries {\n    code\n    country\n  }\n}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/universe/latest/actions/list-stripe-countries?${params}`, {
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
| `query` | string | yes | Universe GraphQL query document to execute for this action. Default: `query ListStripeCountries {\n  availableStripeCountries {\n    code\n    country\n  }\n}`. |
| `variables` | object | no | Optional GraphQL variables object for this query. Default: `{}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Universe API returns.

## Native endpoint

Through the native Universe API, this operation is `POST /graphql` (base URL `https://www.universe.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stripe-countries.md) for the provider-specific parameters and requirements.

