# WeSupply: Get Order Links

Retrieves WeSupply order links for external order IDs.

```
GET https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/get-order-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WeSupply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/get-order-links?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/get-order-links?${params}`, {
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
| `orderExternalOrderIds` | string | no | Comma-separated external order IDs to convert into direct WeSupply order links. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "externalId1": "string",
      "externalId2": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `externalId1` | string | Example direct order link returned by WeSupply. |
| `externalId2` | string | Additional direct order link returned by WeSupply when multiple external order IDs are requested. |

## Native endpoint

Through the native WeSupply API, this operation is `GET /authLinks` (base URL `https://{{credentials.subdomain}}.labs.wesupply.xyz/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-links.md) for the provider-specific parameters and requirements.

