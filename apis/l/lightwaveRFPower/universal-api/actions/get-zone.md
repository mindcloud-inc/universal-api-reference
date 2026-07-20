# LightwaveRF Power: Get Zone

Retrieves a zone from LightwaveRF Power.

```
GET https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/get-zone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LightwaveRF Power `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/get-zone?connectionId=$CONNECTION_ID&zoneId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "zoneId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightwaveRFPower/latest/actions/get-zone?${params}`, {
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
| `zoneId` | string | yes | The LightwaveRF zone identifier to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "groupId": "string",
      "name": "Ava Chen",
      "order": [
        "string"
      ],
      "parentGroups": [
        "string"
      ],
      "subGroups": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `groupId` | string |  |
| `name` | string |  |
| `order` | array<string> |  |
| `parentGroups` | array<string> |  |
| `subGroups` | object |  |
| `type` | string |  |

## Native endpoint

Through the native LightwaveRF Power API, this operation is `GET /v1/zone/{zoneId}` (base URL `https://publicapi.lightwaverf.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-zone.md) for the provider-specific parameters and requirements.

