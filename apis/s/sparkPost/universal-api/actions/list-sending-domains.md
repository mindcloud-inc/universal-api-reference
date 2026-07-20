# SparkPost: List Sending Domains



```
GET https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/list-sending-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparkPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/list-sending-domains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sparkPost/latest/actions/list-sending-domains?${params}`, {
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
| `ownershipVerified` | boolean | no | Filter by verified ownership status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creationTime": "string",
      "domain": "string",
      "isDefaultBounceDomain": true,
      "sharedWithSubaccounts": true,
      "status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationTime` | string |  |
| `domain` | string |  |
| `isDefaultBounceDomain` | boolean |  |
| `sharedWithSubaccounts` | boolean |  |
| `status` | object |  |

## Native endpoint

Through the native SparkPost API, this operation is `GET /sending-domains` (base URL `https://api.sparkpost.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sending-domains.md) for the provider-specific parameters and requirements.

