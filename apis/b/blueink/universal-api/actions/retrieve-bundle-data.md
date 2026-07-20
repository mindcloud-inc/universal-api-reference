# Blueink: Retrieve Bundle Data

Retrieves field data for a Blueink bundle.

```
GET https://connect.mindcloud.co/v1/universal/blueink/latest/actions/retrieve-bundle-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Blueink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blueink/latest/actions/retrieve-bundle-data?connectionId=$CONNECTION_ID&bundleSlug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bundleSlug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blueink/latest/actions/retrieve-bundle-data?${params}`, {
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
| `bundleSlug` | string | yes | Bundle slug to retrieve field data for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "docKey": "string",
      "fieldKey": "string",
      "filledBy": "string",
      "kind": "string",
      "label": "string",
      "packetId": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `docKey` | string |  |
| `fieldKey` | string |  |
| `filledBy` | string |  |
| `kind` | string |  |
| `label` | string |  |
| `packetId` | string |  |
| `value` | string |  |

## Native endpoint

Through the native Blueink API, this operation is `GET /bundles/:bundleSlug/data/` (base URL `https://api.blueink.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-bundle-data.md) for the provider-specific parameters and requirements.

