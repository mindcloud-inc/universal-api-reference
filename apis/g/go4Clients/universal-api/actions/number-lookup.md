# Go4Clients: Number Lookup

Retrieves phone number lookup details from Go4Clients.

```
GET https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/number-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Go4Clients `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/number-lookup?connectionId=$CONNECTION_ID&phoneNumber=573001234501" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phoneNumber": "573001234501"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/go4Clients/latest/actions/number-lookup?${params}`, {
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
| `phoneNumber` | string | yes | Phone number including country code. Example: `573001234501`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "mcc": "string",
      "mnc": [
        [
          "string"
        ]
      ],
      "originalNetwork": "string",
      "ported": true,
      "portedMnc": [
        [
          "string"
        ]
      ],
      "portedNetwork": "string",
      "submittedNumber": "string",
      "succeded": true,
      "transactionDetails": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `mcc` | string |  |
| `mnc[]` | array<string> |  |
| `originalNetwork` | string |  |
| `ported` | boolean |  |
| `portedMnc[]` | array<string> |  |
| `portedNetwork` | string |  |
| `submittedNumber` | string |  |
| `succeded` | boolean |  |
| `transactionDetails` | string |  |

## Native endpoint

Through the native Go4Clients API, this operation is `GET /api/lookup/v1.0/{{phoneNumber}}` (base URL `https://cloud.go4clients.com:8580`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/number-lookup.md) for the provider-specific parameters and requirements.

