# Cloudmersive: Validate State or Province

Validates a state or province in Cloudmersive.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/validate-state-or-province
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/validate-state-or-province?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/validate-state-or-province?${params}`, {
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
| `CountryCode` | string | no | Optional two-letter country code. |
| `CountryFullName` | string | no | Optional country name. |
| `StateOrProvince` | string | no | State or province to validate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "latitude": 1,
      "longitude": 1,
      "stateOrProvince": "string",
      "validState": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `latitude` | number |  |
| `longitude` | number |  |
| `stateOrProvince` | string |  |
| `validState` | boolean |  |

## Native endpoint

Through the native Cloudmersive API, this operation is `POST /validate/address/state` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-state-or-province.md) for the provider-specific parameters and requirements.

