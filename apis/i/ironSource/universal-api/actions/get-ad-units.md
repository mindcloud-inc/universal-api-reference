# ironSource: Get Ad Units

Retrieves ad units from ironSource.

```
GET https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/get-ad-units
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ironSource `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/get-ad-units?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/get-ad-units?${params}`, {
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
| `appKey` | string | no | Application key as seen on the LevelPlay platform. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adFormat": "string",
      "hasAbTest": true,
      "isPaused": true,
      "mediationAdUnitId": "string",
      "mediationAdUnitName": "Ava Chen",
      "reward": {},
      "settings": [
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
| `adFormat` | string | Ad format. |
| `hasAbTest` | boolean | Whether the ad unit has an A/B test. |
| `isPaused` | boolean | Whether the ad unit is paused. |
| `mediationAdUnitId` | string | Mediation ad unit ID. |
| `mediationAdUnitName` | string | Mediation ad unit name. |
| `reward` | object | Reward configuration for rewarded ad units. |
| `settings` | array<object> | Ad unit settings, such as capping, pacing, banner refresh, and test group. |

## Native endpoint

Through the native ironSource API, this operation is `GET levelPlay/adUnits/v1/:appKey` (base URL `https://platform.ironsrc.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ad-units.md) for the provider-specific parameters and requirements.

