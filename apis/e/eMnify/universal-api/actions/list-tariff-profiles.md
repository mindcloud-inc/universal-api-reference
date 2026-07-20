# EMnify: List Tariff Profiles

Retrieves a list of tariff profiles from EMnify.

```
GET https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/list-tariff-profiles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EMnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/list-tariff-profiles?connectionId=$CONNECTION_ID&authToken=Paste%20the%20auth_token%20from%20Retrieve%20Authentication%20Token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "authToken": "Paste the auth_token from Retrieve Authentication Token"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/list-tariff-profiles?${params}`, {
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
| `authToken` | string | yes | Auth token from Retrieve Authentication Token. Example: `Paste the auth_token from Retrieve Authentication Token`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": 1,
      "inclusiveVolume": {
        "multi": true
      },
      "name": "Ava Chen",
      "organisationId": "string",
      "tariff": {
        "created": "2026-05-07T12:00:00.000Z",
        "currency": {
          "code": "string",
          "id": 1,
          "symbol": "string"
        },
        "currencyId": "string",
        "dataBlocksizeId": "string",
        "dataThrottleId": "string",
        "defaultSmsMoRate": 1,
        "defaultSmsMtRate": 1,
        "description": {},
        "id": 1,
        "name": "Ava Chen",
        "organisationId": "string",
        "public": "string",
        "simActivatedRate": 1,
        "simActivationRate": 1,
        "simIssuedRate": 1,
        "simReactivationRate": 1,
        "simSuspendedRate": 1,
        "simSuspensionRate": 1,
        "simTerminationRate": 1,
        "tariffCategoryId": "string",
        "tariffCurrencyCategoryId": "string",
        "tariffStatusId": "string",
        "visibilityId": "string"
      },
      "usedCount": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | number |  |
| `inclusiveVolume.multi` | boolean |  |
| `name` | string |  |
| `organisationId` | string |  |
| `tariff.created` | date |  |
| `tariff.currency.code` | string |  |
| `tariff.currency.id` | number |  |
| `tariff.currency.symbol` | string |  |
| `tariff.currencyId` | string |  |
| `tariff.dataBlocksizeId` | string |  |
| `tariff.dataThrottleId` | string |  |
| `tariff.defaultSmsMoRate` | number |  |
| `tariff.defaultSmsMtRate` | number |  |
| `tariff.description` | object |  |
| `tariff.id` | number |  |
| `tariff.name` | string |  |
| `tariff.organisationId` | string |  |
| `tariff.public` | string |  |
| `tariff.simActivatedRate` | number |  |
| `tariff.simActivationRate` | number |  |
| `tariff.simIssuedRate` | number |  |
| `tariff.simReactivationRate` | number |  |
| `tariff.simSuspendedRate` | number |  |
| `tariff.simSuspensionRate` | number |  |
| `tariff.simTerminationRate` | number |  |
| `tariff.tariffCategoryId` | string |  |
| `tariff.tariffCurrencyCategoryId` | string |  |
| `tariff.tariffStatusId` | string |  |
| `tariff.visibilityId` | string |  |
| `usedCount` | string |  |

## Native endpoint

Through the native EMnify API, this operation is `GET /tariff_profile` (base URL `https://cdn.emnify.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tariff-profiles.md) for the provider-specific parameters and requirements.

