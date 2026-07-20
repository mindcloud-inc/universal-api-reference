# ironSource: Get Mediation Groups

Retrieves mediation groups from ironSource.

```
GET https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/get-mediation-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ironSource `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/get-mediation-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/get-mediation-groups?${params}`, {
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
      "abTest": "string",
      "adFormat": "string",
      "countries": [
        "string"
      ],
      "floorPrice": 1,
      "groupId": "string",
      "groupName": "Ava Chen",
      "instances": [
        {}
      ],
      "mediationAdUnitId": "string",
      "mediationAdUnitName": "Ava Chen",
      "position": 1,
      "segments": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abTest` | string | Related A/B test group. |
| `adFormat` | string | Ad format. |
| `countries` | array<string> | Target country codes. |
| `floorPrice` | number | Minimum bid per impression as CPM. |
| `groupId` | string | Mediation group ID. |
| `groupName` | string | Mediation group name. |
| `instances` | array<object> | Instances configured in the group. |
| `mediationAdUnitId` | string | Ad unit ID to which the group belongs. |
| `mediationAdUnitName` | string | Ad unit name to which the group belongs. |
| `position` | number | Group position in the waterfall list. |
| `segments` | array<string> | Target segment names. |

## Native endpoint

Through the native ironSource API, this operation is `GET levelPlay/groups/v4/:appKey` (base URL `https://platform.ironsrc.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mediation-groups.md) for the provider-specific parameters and requirements.

