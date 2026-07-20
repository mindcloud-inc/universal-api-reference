# LabsMobile: HLR Check

Checks mobile number status and availability with LabsMobile HLR lookup.

```
GET https://connect.mindcloud.co/v1/universal/labsMobile/latest/actions/hlr-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LabsMobile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/labsMobile/latest/actions/hlr-check?connectionId=$CONNECTION_ID&numbers=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "numbers": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/labsMobile/latest/actions/hlr-check?${params}`, {
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
| `numbers` | string | yes | One or more comma-separated phone numbers in E.164 format. |
| `type` | string | no | HLR check type such as status, network, or format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "credits": 1,
      "error": "string",
      "numbers": [
        {}
      ],
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `credits` | number |  |
| `error` | string |  |
| `numbers` | array<object> |  |
| `result` | string |  |

## Native endpoint

Through the native LabsMobile API, this operation is `GET /hlr` (base URL `https://api.labsmobile.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/hlr-check.md) for the provider-specific parameters and requirements.

