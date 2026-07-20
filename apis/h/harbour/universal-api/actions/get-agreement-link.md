# Harbour: Get Agreement Link

Retrieves a specific agreement link from Harbour.

```
GET https://connect.mindcloud.co/v1/universal/harbour/latest/actions/get-agreement-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harbour `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harbour/latest/actions/get-agreement-link?connectionId=$CONNECTION_ID&agreement_link_id=AGREE-1234" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agreement_link_id": "AGREE-1234"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harbour/latest/actions/get-agreement-link?${params}`, {
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
| `agreement_link_id` | string | yes | Unique Harbour agreement link identifier. Example: `AGREE-1234`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agreement_link": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agreement_link` | object |  |

## Native endpoint

Through the native Harbour API, this operation is `GET https://api.harbourshare.com/v1/agreement_links/:agreement_link_id` (base URL `https://api.myharbourshare.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agreement-link.md) for the provider-specific parameters and requirements.

