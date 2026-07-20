# ironSource: Create Application

Creates a new application in ironSource.

```
POST https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/create-application
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ironSource `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/create-application" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/create-application', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `adUnits` | object | no | Optional ad unit status object, for example {"RewardedVideo":"Live","Interstitial":"Live","OfferWall":"Off","Banner":"Live","NativeAd":"Live"}. |
| `appName` | string | no | Application name. Required for apps that are not live in the store. |
| `ccpa` | number | no | Optional CCPA status as an integer: 1 for true, 0 for false. |
| `coppa` | number | no | COPPA status as an integer: 1 for true, 0 for false. |
| `platform` | string | no | Operating system for a non-live app: iOS or Android. |
| `storeUrl` | string | no | Store URL for a live app. |
| `taxonomy` | string | no | Application sub-genre for a live app. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appKey": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appKey` | string | Created Unity LevelPlay application key. |

## Native endpoint

Through the native ironSource API, this operation is `POST partners/publisher/applications/v6` (base URL `https://platform.ironsrc.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-application.md) for the provider-specific parameters and requirements.

