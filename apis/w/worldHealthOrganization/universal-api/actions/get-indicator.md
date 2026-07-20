# World Health Organization: Get Indicator

Retrieves an indicator from the World Health Organization.

```
GET https://connect.mindcloud.co/v1/universal/worldHealthOrganization/latest/actions/get-indicator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a World Health Organization `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldHealthOrganization/latest/actions/get-indicator?connectionId=$CONNECTION_ID&indicatorCode=WHOSIS_000001" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "indicatorCode": "WHOSIS_000001"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worldHealthOrganization/latest/actions/get-indicator?${params}`, {
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
| `indicatorCode` | string | yes | WHO indicator code, such as WHOSIS_000001. Example: `WHOSIS_000001`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "IndicatorCode": "string",
      "IndicatorName": "Ava Chen",
      "Language": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `IndicatorCode` | string |  |
| `IndicatorName` | string |  |
| `Language` | string |  |

## Native endpoint

Through the native World Health Organization API, this operation is `GET /Indicator(':indicatorCode')` (base URL `https://ghoapi.azureedge.net/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-indicator.md) for the provider-specific parameters and requirements.

