# Trolley: List Verifications

Retrieves all verification records from Trolley.

```
GET https://connect.mindcloud.co/v1/universal/trolley/latest/actions/list-verifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trolley `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trolley/latest/actions/list-verifications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trolley/latest/actions/list-verifications?${params}`, {
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
| `verificationType` | string | no | Verification type |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {},
      "ok": true,
      "verifications": [
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
| `meta` | object |  |
| `ok` | boolean |  |
| `verifications` | array<object> |  |

## Native endpoint

Through the native Trolley API, this operation is `GET /v1/verifications` (base URL `https://api.trolley.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-verifications.md) for the provider-specific parameters and requirements.

