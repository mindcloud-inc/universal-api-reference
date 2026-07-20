# RapidReg: List Registrations

Retrieves registrations from RapidReg.

```
GET https://connect.mindcloud.co/v1/universal/rapidReg/latest/actions/list-registrations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RapidReg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rapidReg/latest/actions/list-registrations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rapidReg/latest/actions/list-registrations?${params}`, {
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
| `brandId` | string | no | Optional brand UUID to filter registrations. |
| `itemId` | string | no | Optional item UUID to filter registrations. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `start` | number | no | Optional UTC timestamp lower bound. |
| `end` | number | no | Optional UTC timestamp upper bound. |
| `limit` | number | no | Optional maximum number of registrations to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "registrations": [
        {}
      ],
      "results": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `registrations` | array<object> | Registration objects. |
| `results` | number | Number of registration records returned. |
| `success` | boolean | Whether the request was successful. |

## Native endpoint

Through the native RapidReg API, this operation is `POST /api/v1/get/registrations` (base URL `https://rapidreg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-registrations.md) for the provider-specific parameters and requirements.

