# Dwolla: Get Funding Source

Retrieves details for a funding source from Dwolla.

```
GET https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/get-funding-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dwolla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/get-funding-source?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dwolla/latest/actions/get-funding-source?${params}`, {
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
| `id` | string | no | Dwolla funding source ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "bankAccountType": "string",
      "bankName": "Ava Chen",
      "channels": [
        "string"
      ],
      "created": "string",
      "id": "string",
      "name": "Ava Chen",
      "removed": true,
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object | HAL links for related funding-source resources. |
| `bankAccountType` | string | Bank-account subtype when the funding source is a bank account. |
| `bankName` | string | Name of the backing financial institution. |
| `channels` | array<string> | Transfer channels available for the funding source. |
| `created` | string | Funding-source creation timestamp. |
| `id` | string | Dwolla funding source identifier. |
| `name` | string | Display name of the funding source. |
| `removed` | boolean | Whether the funding source has been removed. |
| `status` | string | Current Dwolla funding-source status. |
| `type` | string | Dwolla funding-source type. |

## Native endpoint

Through the native Dwolla API, this operation is `GET /funding-sources/[:id]` (base URL `https://api-sandbox.dwolla.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-funding-source.md) for the provider-specific parameters and requirements.

