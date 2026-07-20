# UniOne: Get Suppression

Retrieves suppression details from UniOne by email address.

```
GET https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/get-suppression
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UniOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/get-suppression?connectionId=$CONNECTION_ID&email=wizard-suppression-20260402%40mindcloud.co" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "wizard-suppression-20260402@mindcloud.co"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/get-suppression?${params}`, {
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
| `email` | string | yes | Email address to look up in the suppression list. Example: `wizard-suppression-20260402@mindcloud.co`. |
| `allProjects` | boolean | no | Whether to search across all projects for this email. Default: `false`. Example: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UniOne API returns.

## Native endpoint

Through the native UniOne API, this operation is `POST suppression/get.json` (base URL `https://api.unione.io/en/transactional/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-suppression.md) for the provider-specific parameters and requirements.

